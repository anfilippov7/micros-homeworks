# Домашнее задание к занятию «Введение в микросервисы»

## Задача

Руководство крупного интернет-магазина, у которого постоянно растёт пользовательская база и количество заказов, рассматривает возможность переделки своей внутренней   ИТ-системы на основе микросервисов. 

Вас пригласили в качестве консультанта для оценки целесообразности перехода на микросервисную архитектуру. 

Опишите, какие выгоды может получить компания от перехода на микросервисную архитектуру и какие проблемы нужно решить в первую очередь.


## Решение

# Выгоды которые может получить компания от перехода на микросервисную архитектуру:

 - микросервисы хорошо подходят для разработки больших и сложных систем;
 - более простое развертывание, микросервисы позволяют развертывать каждый отдельный сервис независимо, бдагодаря небольшим изменениям мы получаем существенное увеличение надежности всей системы, при возникновении проблем гораздо проще откатить изменения;
 - возможность использования различных технологии в рамках одного проекта (позволяет применять наиболее подходящий инструмент для конкретной бизнес-задачи); 
 - новая функциональность попадает к пользователям гораздо чаще (возможность быстро внедрить мелкие исправления и улучшения а также быстрое тестирование и быстрые циклы обновления и повторного развертывания);
 - простота замены, благодаря небольшому размеру микросервис проще переписывать на другой язык программирования;
 - легкая масштабируемость, сервисы распределяются между серверами в зависимости от потребностей;
 - ситема построенная на микросервисах более устойчива к ошибкам, а также включает большое количество техник по работе с ошибками;
 - микросервисная архитектура позволяет внедрять новые технологии для отдельных частей системы;
 - микросервисная архитектура позволяет исключить простои при обновлении сервиса;
 - возможность выборочного масштабирования необходимых компонентов или функций сервиса;
 - воспроизводимость проета практически в любых средах;
 - микросервисная архитектура позволяет организовать разделение на команды по компетенциям и зонам ответственности;
 - возможность более подробного мониторинга системы.


# Недостатки:

 - большое количество сервисов за которыми нужно следить и которыми нужно управлять;
 - необходима ситема сбор логов, т.к. без нее невозможно найти причины возникновения ошибок или разобрать особенности поведения системы;
 - более сложное управление настойками ситемы;
 - более сложное управление инфраструктурой; 
 - необходимо большое внимание уделять обратной и прямой совместимости api, нельзя допускать чтобы релиз одного сервиса зависел от релиза другого или требовал обновления клиента;
 - необходимо четкое понимание какие версии каких сервисов обрабатывают запросы пользователей и какие библиотеки используются;
 - необходимо уделять достаточное внимание автоматизации рутинных операций, это ключ к сокращению от ошибок и постоянной актуализации документации, нужно недопускать публикацию непроверенных артефактов.
 - нужно иметь актуальную документацию о возможностях каждого сервиса и доступных методах api и правилах его использования
 - необходимость шаблонов и скриптов быстрого создания сервисов, нужен пакетный репозитории для распространения общих библиотек и модулей.


# Проблемы которые необходимо будет решить в первую очередь:

 - при разбиении монолита на микросервисы возможно придется переписать весь код;
 - необходимо определить бизнес-цели каждого сервиса;
 - возможно некоторое снижение производительности;
 - усложнение сопровождения из-за увеличивающейся инфраструктуры;
 - управление версиями при большом количестве сервисов;
 - определение инструментов мниторинга и логирования, резервного копирования и управления.
