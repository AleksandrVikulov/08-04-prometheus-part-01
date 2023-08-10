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
<p></p>---

### Задание 2

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

---

### Задание 3

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

---

## Дополнительные задания (со звездочкой*)

Эти задания дополнительные (не обязательные к выполнению) и никак не повлияют на получение вами зачета по этому домашнему заданию. Вы можете их выполнить, если хотите глубже и/или шире разобраться в материале.

### Задание 4* со звездочкой

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
