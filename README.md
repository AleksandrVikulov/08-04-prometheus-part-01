# Домашнее задание к занятию "`Система мониторинга Prometheus`" - `Викулов Александр`

### Задание 1

Процесс выполнения

1. Создаем пользователя Prometheus.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task01-img01.png">
</kbd>
<p></p>

2. Скачиваем последнюю версию Prometheus для конкретной системы.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task01-img02.png">
</kbd>
<p></p>

3. Извлечем содержимое архива.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task01-img03.png">
</kbd>
<p></p>

4. Создадим рабочие директории `/etc/prometheus` и `/var/lib/prometheus`.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task01-img04.png">
</kbd>
<p></p>

5. Скопируем директории и файлы prometheus в нужные папки:

* Скопируем файлы `prometheus` и `promtool` в директорию `/usr/local/bin`

* Скопируем папку `console_libraries` в директорию `/etc/prometheus`

* Скопируем папку `consoles` в директорию `/etc/prometheus`

* Скопируем конфигурационный файл `prometheus.yml` в директорию `/etc/prometheus`

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task01-img05.png">
</kbd>
<p></p>

6. Передадим права управления файлами и папками пользователю prometheus.

* Для папок `/etc/prometheus` и `/var/lib/prometheus`
* Для файлов `/usr/local/bin/prometheus` и `/usr/local/bin/promtool`

Убедимся, что права переданы.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task01-img06.png">
</kbd>
<p></p>

7. Проверим работоспособность Prometheus

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task01-img07-1.png">
</kbd>
<p></p>

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task01-img07-2.png">
</kbd>
<p></p>

8. Начнем настройку сервиса для запуска и работы Prometheus.
   Для начала создадим файл `prometheus.service`, который будет отвечать за запуск сервиса.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task01-img08.png">
</kbd>
<p></p>

9. Откроем файл для редактирования и добавим туда настройки сервиса.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task01-img09.png">
</kbd>
<p></p>

10. Запустим сервис через systemctl и убедимся, что все работает.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task01-img10-1.png">
</kbd>
<p></p>

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task01-img10-2.png">
</kbd>
<p></p>

---

### Задание 2

Процесс выполнения

1. Скачаем версию Node Exporter для нашей операционной системы.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task02-img01.png">
</kbd>
<p></p>

2. Распакуем архив.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task02-img02.png">
</kbd>
<p></p>

3. Запускаем Node Exporter, проверяем, что все работает

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task02-img03-1.png">
</kbd>
<p></p>

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task02-img03-2.png">
</kbd>
<p></p>

4. Начнем подготовку к созданию сервиса для запуска Node Exporter
   Для этого вначале переместим требуемые файлы в нужные папки:

   * Создадим папку `/etc/prometheus/node-exporter`
   * Скопируем туда файл `node_exporter`
   * Передадим право управления пользователю prometheus

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task02-img04.png">
</kbd>
<p></p>

5. Создадим файл с сервисом `node-exporter.service`

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task02-img05.png">
</kbd>
<p></p>

6. Откроем файл для редактирования и добавим туда настройки сервиса.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task02-img06.png">
</kbd>
<p></p>

7. Запустим сервис через systemctl и убедимся, что все работает.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task02-img07-1.png">
</kbd>
<p></p>

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task02-img07-2.png">
</kbd>
<p></p>


---

### Задание 3

Процесс выполнения

1. Откроем на редактирование файл `/etc/prometheus/prometheus.yml`

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task03-img01.png">
</kbd>
<p></p>

2. Добавим в файл в качестве таргета адрес, по которому можно обратиться к Node Exporter.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task03-img02.png">
</kbd>
<p></p>

3. Перезапустим Prometheus, проверим, что он работает после перезапуска.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task03-img03.png">
</kbd>
<p></p>

4. Перейдем в GUI на локалхосте, посмотрим раздел `targets` и увидим, что появился наш Node Exporter появился как новый таргет на порту 9100.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task03-img04.png">
</kbd>
<p></p>

5. По предыдущему скриншоту видно, что таргет перешел в статус `UP` и prometheus оправшивает наш endpoint.

---

## Дополнительные задания (со звездочкой*)

Эти задания дополнительные (не обязательные к выполнению) и никак не повлияют на получение вами зачета по этому домашнему заданию. Вы можете их выполнить, если хотите глубже и/или шире разобраться в материале.

### Задание 4* со звездочкой

1. Зайдем на официальный сайт Grafana в раздел загрузок и посмотрим рекоменадции по установке на нашу систему.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task04-img01.png">
</kbd>
<p></p>

2. Установим утилиты `adduser` и `libfontconfig` (они и так были последнее версии).

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task04-img02.png">
</kbd>
<p></p>

3. Скачаем deb-пакет с последним релизом Grafana.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task04-img03.png">
</kbd>
<p></p>

4. Установим.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task04-img04.png">
</kbd>
<p></p>

5. Добавляем в автозапуск и запускаем Grafana, проверяем, что всё работает.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task04-img05.png">
</kbd>
<p></p>

6. Заходим к графану на 3000 порт.

<p></p>
<kbd>
  <img src="https://github.com/AleksandrVikulov/08-04-prometheus-part-01/blob/master/img/task04-img06.png">
</kbd>
<p></p>

---

### Задание 5* со звездочкой

Процесс выполнения

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.
