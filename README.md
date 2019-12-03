# manual_kernel_update
Kernel update. Create custom box for Vagrant Clound. Packer.
#
---
## Домашнее задание 
---
###  Часть №1 Part#1

Согласно задания была создана виртуальная машина из приложеного Vagrant файла. Вручную были произведены настройки системы и было установлено новое ядро из репозитория elrepo-kernel.

---
#### Сдача задания

- Создаём с помощью Packer автоматизированный образ с использованием скриптов
- Публикуем полученный box в Vagrant Cloud
- Модифицируем файл Vagrant для скачивания готового обрзаза из Vagrant Cloud

---
### Часть №2 Part#2

Сборка ядра из исходных файлов.

Скачиваем исходники ядра с сайта kernel.org
```
https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-5.4.tar.xz
```
Устанавливаем необходимые пакеты для сборки ядра из исходников.

`sudo yum install ncurses-devel bison flex elfutils-libelf-devel openssl-devel bc gcc wget perl`


> Для того, чтобы ядро собиралось быстрее увеличиваем память до 2048 mb  и количества vcpu до 4

---
#### Сдача задания
#####   Вариант №1

- Создаём с помощью Packer автоматизированный образ с использованием скриптов
- Публикуем полученный box в Vagrant Cloud
- Модифицируем файл Vagrant для скачивания готового обрзаза из Vagrant Cloud
<details>
<summary>Вариант №2</summary>

В Vagrantfile добавлена секция provision. Обновление ядра происходит во время создания виртуальной машины. Результат - Новое ядрро из исходников после перезагрузки
</details>

