# Stelmakh - клавиатура с тачпадом и NiceView дисплеем

![Клавиатура](src/2025-12-05%2016.48.54.jpg)

Более подробно про создание этой клавиатуры я писал вот в этой статье на Хабре (https://habr.com/p/982192/)

За детальной информацией, обращайтесь ко мне в телеграм: https://t.me/StelmakhDigital

## Корпуса для печати

![Full_case_STELMAKH_keyboard_v5](Case/Full_case_STELMAKH_keyboard_v5.3mf)

Stelmakh корпус (такая же как на фото сверху): (Case/Full_case_STELMAKH_keyboard_v5.3mf)

![Full_case_SOFLE_keyboard_v1.3mf](Case/Full_case_SOFLE_keyboard_v1.3mf)

Sofle V1 корпус: (Case/Full_case_SOFLE_keyboard_v1.3mf)

## Схема клавиш

![Keymaps](keymap-drawer/stelmakh.svg)


## Сборка прошивки локально

Написал Make команды для удобства:

---

Подготовка среды:

```bash
make start
source ./env_activate.sh
```

Все, west и зависимости установлены и готовы для сборки прошивки.

Сборка:

```bash
make _build_reset
make _build_l
make _build_r
```

или 

```bash
make all
```

> Будет собрано 3 прошивки. Reset прошивку закидывайте перед прошивкой (левой или правой соответственно)

---

Для просмотра дополнительных команд:

```bash
make help
```


## Сборка прошивки через Github Actions

Достаточно сделать форк этого репозитория и запушить необходимые изменения. 

Прошивки будут собраны автоматически в архиве - в пунке `Actions` вашего репозитория.