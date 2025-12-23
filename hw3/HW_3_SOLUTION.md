# Решение домашнего задания №3
*автор*: Продьма Илья Дмитриевич МКС244

## Вывод patronictl - статусы хостов
![вывод patronictl](img/img1.png)

## Вывод haproxy на localhost:7001
![вывод haproxy](img/img2.png)

## Подключение к master-node БД и создание объектов
![psql](img/img3.png)

## Запуск генерации трафика
![traffic_generator.py](img/img4.png)

## Изменения в БД при генерации
![db rows changed](img/img5.png)

## Распределение трафика на хостах patroni
![patroni traffic](img/img6.png)

## Выключение лидера demo-patroni3
docker stop demo-patroni3
![patroni change master](img/img7.png)

## Новое состояние хостов
![вывод patronictl](img/img8.png)

## Выключение реплики demo-patroni1
docker stop demo-patroni1
![Переходное состояние](img/img9.png)

![Только demo-patroni2](img/img10.png)

## Включение реплик demo-patroni1 и demo-patroni3
docker start demo-patroni1
docker start demo-patroni3

![Включение реплик](img/img11.png)


## Отключение etcd (лидер)
docker stop demo-etcd2
![отключение etcd2](img/img12.png)

## Отключение etcd (реплика)
docker stop demo-etcd1
![отключение etcd1](img/img13.png)

влияние на генерацию трафика:
![traffic change](img/img14.png)

вывод haproxy:
![haproxy after etcd off](img/img15.png)

вывод patronictl после запуска etcd:
![patronictl after etcd on](img/img16.png)


## Отключение haproxy
docker stop haproxy
![отключение haproxy](img/img17.png)

влияние на генерацию трафика:
![traffic change](img/img18.png)



