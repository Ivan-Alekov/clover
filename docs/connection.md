Подключение PixHawk/PixRacer к Raspberry Pi
===

Для программирования [автономных полетов](/docs/simple_offboard.md), [работы с PixHawk по Wi-Fi](/docs/gcs_bridge.md), использования [веб-пульта](/docs/web_rc.md) и других функций необходимо подсоединить Raspberry Pi к PixHawk.

Подключение по USB
---

Соедините PixHawk/PixRacer и Raspberry Pi PX4 Micro-USB to USB кабелем.

Необходимо убедиться, что в launch-файле Клевера (`~/catkin_ws/src/clever/clever/clever.launch`) тип подключения установлен на USB:

```xml
<arg name="fcu_conn" default="usb"/>
```

При изменении launch-файла необходимо перезапустить пакет `clever`:

```bash
sudo systemctl restart clever
```

Подключение по UART
---

TODO

Необходимо убедиться, что в launch-файле Клевера (`~/catkin_ws/src/clever/clever/clever.launch`) тип подключения установлен на UART:

```xml
<arg name="fcu_conn" default="uart"/>
```

При изменении launch-файла необходимо перезапустить пакет `clever`:

```bash
sudo systemctl restart clever
```