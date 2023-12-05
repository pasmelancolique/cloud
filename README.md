---
description: pew pew pew pew pew
---
# Отчёт Аналитическая лабораторная работа №1

## Состав команды
* Холод Виолетта https://t.me/maybevilou
* Сергеев Артём https://t.me/imrreyz
* Морозов Матвей 	https://t.me/jkkgmr
* Копытко Александр https://t.me/monegasquee

## Цель работы
Знакомство с облачными сервисами. Понимание уровней абстракции над инфраструктурой в облаке. Формирование понимания типов потребления сервисов в сервисной-модели. Сопоставление сервисов между разными провайдерами.

## Дано
1. Слепок данных биллинга от провайдера после небольшой обработки в виде SQL-параметров. Символ % в начале/конце означает, что перед/после него может стоять любой набор символов.
2. Google с документациями провайдера

## Исходные данные
<img src="">

## Описание сервисов

### Amazon Redshift
Amazon Redshift - полностью управляемый сервис хранения и анализа данных в облаке. Построен на базе архитектуры MPP (Massively Parallel Processing), позволяющей эффективно обрабатывать большие объемы данных. Предоставляет высокую производительность для выполнения сложных запросов SQL и поддерживает интеграцию с различными инструментами бизнес-аналитики.

### AWS Directory Service
AWS Directory Service - управляемый сервис, предоставляющий службу каталогов для централизованного управления идентификацией и доступом к ресурсам в сети. Поддерживает интеграцию с Microsoft Active Directory и LDAP-каталогами, обеспечивая единое управление пользователями и группами.

### Amazon Glacier
Amazon Glacier - надежный и низкозатратный облачный сервис для долгосрочного хранения данных. Предназначен для архивирования и резервного копирования данных, которые редко используются. Обеспечивает надежность и безопасность данных при соблюдении требований по долгосрочному хранению.

### Amazon S3
Amazon S3 - простой и масштабируемый облачный сервис для хранения и передачи данных. Предоставляет высокую доступность, долгосрочное хранение, а также возможности для создания статических веб-сайтов и интеграции с другими сервисами AWS.

### Amazon SNS
Amazon Simple Notification Service (SNS) - масштабируемый и гибкий сервис для отправки уведомлений и сообщений. Обеспечивает интеграцию с различными конечными точками, включая электронную почту, пуш-уведомления и SMS. Поддерживает как взаимодействие между приложениями (A2A), так и уведомления конечным пользователям (A2P).

### Amazon Translate
Amazon Translate - сервис машинного перевода, предоставляющий API для автоматического перевода текстов на различные языки. Обеспечивает быстрый и точный перевод, поддерживая интеграцию с приложениями и веб-сайтами. 

### Amazon Transcribe
Amazon Transcribe - автоматический сервис распознавания речи, который преобразует аудио-записи в текст. Поддерживает различные форматы аудио и обеспечивает точность распознавания для создания текстовых данных из аудио-контента.

### AWS Code Pipline
AWS CodePipeline - полностью управляемый сервис для автоматизации процессов непрерывной поставки (CI/CD). Обеспечивает создание, тестирование и развертывание кода с использованием гибких конвейеров, интеграцию с различными инструментами разработки.

### AWS Code Build
AWS CodeBuild - сервис для сборки и тестирования кода автоматически. Обеспечивает масштабируемую инфраструктуру для сборки приложений, поддерживает различные языки программирования и интеграцию с другими сервисами AWS.

### Amazon ML
Amazon ML - сервис машинного обучения, предоставляющий возможности создания, обучения и развертывания моделей машинного обучения без необходимости глубокого понимания алгоритмов.

### Amazon Polly
Amazon Polly - сервис текстового воспроизведения, использующий технологии генерации речи. Позволяет создавать высококачественные звучащие голоса для интеграции с приложениями и устройствами.

## Маппинг
После изучения AWS и Yandex Cloud был произведён маппинг сервисов.
|  Amazon                     | Yandex Cloud                             |
|-----------------------------|------------------------------------------|
| Amazon Redshift             | Yandex Managed Data Warehouse            |
| AWS Directory Service       | Yandex Identity and Access Management    |
| Amazon Glacier              | Yandex Object Storage (Cloud Storage)    |
| Amazon S3                   | Yandex Object Storage (Cloud Storage)    |
| Amazon SNS                  | Yandex Message Queue (MQ)                |
| Amazon Translate            | Yandex Translate API                     |
| Amazon Transcribe           | Yandex SpeechKit (Speech-to-Text API)    |
| AWS CodePipeline            | Yandex Cloud CI/CD                       |
| CodePipeline                | Yandex Cloud CI/CD                       |
| Amazon Machine Learning     | Yandex AI Platform                       |
| Amazon Polly                | Yandex SpeechKit (Text-to-Speech API)    |

## Возможность миграции
Исходя из проведенного маппинга сервисов между AWS и Yandex Cloud, можно сделать следующие общие выводы:
### Близкие аналогии:
Некоторые сервисы имеют довольно близкие аналогии между AWS и Yandex Cloud, такие как Amazon S3 и Yandex Object Storage, Amazon SNS и Yandex Message Queue, а также AWS CodePipeline и Yandex Cloud CI/CD. Это облегчит процесс миграции, поскольку аналогичные функции предоставляются обоими облачными провайдерами.
### Вынужденное комбинирование сервисов:
В ряде случаев может потребоваться комбинирование нескольких сервисов Yandex Cloud для полного соответствия функциональности сервисам AWS. Это может включать в себя использование нескольких инструментов для достижения аналогичных целей.
### Адаптация
В процессе миграции может потребоваться адаптация конфигураций и кодов базы данных, особенно если используются специфические функции или API, которые могут отличаться между облачными провайдерами.
## Мини вывод
Миграция между облачными провайдерами, такими как AWS и Yandex Cloud, может быть сложным процессом из-за различий в архитектуре, сервисах и API. В целом, успешная миграция зависит от тщательного планирования, тестирования и адаптации с учетом специфики каждого сервиса. Важно также взаимодействие с командой разработчиков и администраторов для обеспечения плавного перехода и минимизации возможных проблем.
