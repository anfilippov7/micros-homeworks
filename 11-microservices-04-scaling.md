
# Домашнее задание к занятию «Микросервисы: масштабирование»

Вы работаете в крупной компании, которая строит систему на основе микросервисной архитектуры.
Вам как DevOps-специалисту необходимо выдвинуть предложение по организации инфраструктуры для разработки и эксплуатации.

## Задача 1: Кластеризация

Предложите решение для обеспечения развёртывания, запуска и управления приложениями.
Решение может состоять из одного или нескольких программных продуктов и должно описывать способы и принципы их взаимодействия.

Решение должно соответствовать следующим требованиям:
- поддержка контейнеров;
- обеспечивать обнаружение сервисов и маршрутизацию запросов;
- обеспечивать возможность горизонтального масштабирования;
- обеспечивать возможность автоматического масштабирования;
- обеспечивать явное разделение ресурсов, доступных извне и внутри системы;
- обеспечивать возможность конфигурировать приложения с помощью переменных среды, в том числе с возможностью безопасного хранения чувствительных данных таких как пароли, ключи доступа, ключи шифрования и т. п.

Обоснуйте свой выбор.

## Решение 1

Таблица возможностей различных решений для обеспечения развёртывания, запуска и управления приложениями:

|Необходимые требования                                                         |Docker Swarm|Kubernetes|OpenShift|
|:-----------------------------------------------------------------------------:|:----------:|:--------:|:-------:|
|поддержка контейнеров                                                          | +          | +        |  +      | 
|Обеспечение обнаружения сервисов и маршрутизация запросов                      | +          | +        |  +      | 
|обеспечение возможности горизонтального масштабирования                        | +          | +        |  +      | 
|обеспечение возможности автоматического масштабирования                        | -          | +        |  +      |
|обеспечение явного разделения ресурсов, доступных извне и внутри системы       | +          | +        |  +      |
|обеспечение возможности конфигурировать приложения с помощью переменных среды  | +          | +        |  +      |



 - В случае необходимости развертывания приложений, содержащих относительно небольшое количество микросервисов, целесообразно воспользоваться Docker Swarm
Docker Swarm использует docker compose файлы, которые сильно распространены и можно найти множество готовых решений для различных задач и доработать.
При расширении приложения можно осуществить лёгкий переход на использование Kubernetes (при необходимости более серьёзной оркестрации).

 - В случае необходимости развертывания приложений, содержащих большое количество микросервисов, целесообразно воспользоваться Kubernetes
Kubernetes управляет и запускает контейнеры Docker на большом количестве хостов, а так же обеспечивает совместное размещение и репликацию большого количества контейнеров. Продукт имеет широкое распространение, что облегчает поддержку данному решению.
Покрывает все необходимые требования при использовании микросервисной архитектуры

 - В случае необходимости использования полноценной платформы для разработки, развертывания и эксплуатации классических и контейнерных приложений в физических, виртуальных и общедоступных облачных средах, целесообразно воспользоваться OpenShift
OpenShift работает с Kubernetes что позволяет совершить лёгкий переход.
Имеет ряд решений и инструментов для CI/CD, хранения логов, мониторинга и пр.
Является цельным решением для разработки приложения использующего микросервисную архитектуру так содержит уже готовые решения.


## Задача 2: Распределённый кеш * (необязательная)

Разработчикам вашей компании понадобился распределённый кеш для организации хранения временной информации по сессиям пользователей.
Вам необходимо построить Redis Cluster, состоящий из трёх шард с тремя репликами.

### Схема:

![11-04-01](https://user-images.githubusercontent.com/1122523/114282923-9b16f900-9a4f-11eb-80aa-61ed09725760.png)

---

### Как оформить ДЗ?

Выполненное домашнее задание пришлите ссылкой на .md-файл в вашем репозитории.

---
