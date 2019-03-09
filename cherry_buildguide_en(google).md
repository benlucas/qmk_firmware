# Build Guide

This is Corne Cherry's build guide.
[Corne Chocolate はこちら](https://github.com/foostan/crkbd/blob/master/corne-chocolate/doc/buildguide_jp.md)。


## Parts
### Have to
| Name | Count | Notes | 
|:-|:-|:-|
| PCB | 2枚 | |
| トッププレート | 2枚 | |
| ボトムプレート | 2枚 | PCBタイプとアクリルタイプが選べます |
| ProMicro保護プレート | 2枚 | |
| ProMicro | 2枚 | |
| TRRSジャック | 2個 | |
| タクトスイッチ | 2個 | |
| ダイオード | 42本 | チップ部品のみに対応 |
| Kailh PCBソケット | 42個 | |
| キースイッチ | 42個 | CherryMX互換にのみ対応 |
| キーキャップ | 42個 | 1u 40個、1.5u 2個 |
| OLEDモジュール | 2枚 | |
| ピンヘッダ 4連 | 2つ | |
| ピンソケット4連 | 2つ | |
| スペーサー M2 6.5mm | 10本 | |
| スペーサー M2 8mm | 4本 | |
| ネジ M2 4mm | 28本 | |
| クッションゴム | 8個 | |
| TRS(3極)ケーブル | 1本 | TRRS(4極)ケーブルでも可 |
| Micro USBケーブル | 1本 | |

### オプション
| Name | Count | Notes |
|:-|:-|:-|
| SK6812MINI | 54個 | 上向き実装 42個、下向き実装 12個 |

![01](https://user-images.githubusercontent.com/736191/46775572-c3202700-cd42-11e8-8097-9daa71bccc98.JPG)

## Advance preparation
Although there is work to put the farm in ProMicro in the middle of implementation, it is a time-consuming matter to prepare the environment for building the farm, so we recommend you to get started at the beginning.
https://docs.qmk.fm/#/newbs_getting_started We refer to here and install the necessary ones according to the OS (it takes time to install and it is efficient to proceed with implementation while moving).

## Implementation

Since the PCB is reversible, first decide which one to use for left / right.

![02](https://user-images.githubusercontent.com/736191/46775606-024e7800-cd43-11e8-8792-90b0c3c9d060.JPG)

### Diode

We will solder diodes of chip parts.
It is free to install on either side, but in this build guide we will install it on the back side.

Since the chip parts are very small, working with tweezers and reverse action tweezers becomes easier.
** Since the orientation of the diodes is fixed **, arranging the rows and rows and the diodes in advance aligned in advance as shown in the next picture can proceed smoothly.

![03](https://user-images.githubusercontent.com/736191/46775611-04b0d200-cd43-11e8-8f73-919256c0064d.JPG)

The direction of the diode is as follows. Attach the "|||" of the chip part so that it faces the "|" of the diode mark "| ◁". 

![04](https://user-images.githubusercontent.com/736191/46775614-08dcef80-cd43-11e8-907c-7fc853d06b8b.JPG)

It is a trick to attach chip parts, but first solder as a spare solder only on the right side of the pad.

![05](https://user-images.githubusercontent.com/736191/46775615-09758600-cd43-11e8-9fa4-c78af441bb6f.JPG)

Then solder one leg of the diode so that the spare solder is melted.
At this time, using reverse action tweezers makes it possible to hold the chip parts firmly without applying force, so it is recommended as it can concentrate on alignment and soldering.
Also, if the soldering iron is too hot or you touch the solder too much, the flux contained in the solder will vaporize and there is a possibility that a mountain of solder will be clean, but since it can be repaired later, it is only conscious of attaching the parts at this point I am okay.

![06](https://user-images.githubusercontent.com/736191/46775616-09758600-cd43-11e8-9cc5-c4f5e49dc578.JPG)

It is okay if the diode is not floating from the side when one leg is attached. If it floats, it will be clean if you heat the part soldered again with a soldering iron while pressing the diode with tweezers or fingers.

![07](https://user-images.githubusercontent.com/736191/46775618-09758600-cd43-11e8-8305-83972952d307.JPG)

Next, solder the other side. A small amount of solder is enough, so pay attention to overturning.
If you put too much, you can take it with suction wire or scoop with a soldering iron.

Also, if the amount of solder on the preliminary solder side is small, add soldering in addition, if you are in the mountain it will be clean if you heat the flux from above.

![08](https://user-images.githubusercontent.com/736191/46776208-93bee980-cd45-11e8-82e2-db25e1070ef4.JPG)

### TRRS jack, reset switch

Solder the TRRS jack and reset switch to the surface of the PCB as shown below.
In this build guide, since the diode is attached to the backside, it becomes the opposite side.

![09](https://user-images.githubusercontent.com/736191/46775620-0a0e1c80-cd43-11e8-92b4-99a3d63caa16.JPG)

### Jumper and pin socket for OLED module
To use the OLED module, jump as follows.
Please also ** Please jumper only the surface **.

Also solder the pin socket on the same side.

![10](https://user-images.githubusercontent.com/736191/46775621-0a0e1c80-cd43-11e8-9ef3-c5c01879eb90.JPG)

If the jumper does not go well, perhaps the amount of solder is low or the flux contained in the solder has evaporated.
In that case, if you use more solder or apply a separate flux, you can jumper well.

### ProMicro
Solder the pin header so that it fits into the white frame and solder it with the back side of ProMicro side up.

![11](https://user-images.githubusercontent.com/736191/46775622-0a0e1c80-cd43-11e8-9910-49b81db92c02.JPG)
![12](https://user-images.githubusercontent.com/736191/46775623-0aa6b300-cd43-11e8-826c-d6422070ddea.JPG)

In addition, please refer to [Helix Build Guide] (https://github.com/MakotoKurauchi/helix/blob/master/Doc/buildguide_jp.md#pro-micro) when using spring pin header.

### OLED module
Insert the pin header first into the pin socket for OLED, then solder the pin header and OLED module.
Since the OLED module is easy to float at this time, be careful not to float while pressing down with the finger.

![13](https://user-images.githubusercontent.com/736191/46775624-0aa6b300-cd43-11e8-8f83-7acc5e0a407c.JPG)
![14](https://user-images.githubusercontent.com/736191/46775627-0aa6b300-cd43-11e8-8849-ba0d776692e3.JPG)

### Action confirmation
We recommend checking the operation when ProMicro and OLED modules are attached (it is difficult to isolate the problem at the very end).

If you want to check the operation, please refer to the "Firmware" section below first and insert the firmware for crkbd into ProMicro (be sure to put it on both sides).

To check the operation, connect the left side with the PC with MicroUSB, connect the left side and the right side with the TRS cable and do it. Since there are defects such as jack etc., please be sure to check the operation after connecting the left and right, not one by one. If this is done correctly, if you short the pad to attach the PCB socket with tweezers or the like, the key pressed on the OLED module will be displayed.

![15](https://user-images.githubusercontent.com/736191/46775628-0b3f4980-cd43-11e8-96d1-59b20da62e5b.JPG)

### Kailh PCB socket
Fill solder on pads on both sides of the back side. Please add a lot beforehand because it is difficult to add later.

![16](https://user-images.githubusercontent.com/736191/46775629-0b3f4980-cd43-11e8-83e2-ca51572f95d0.JPG)

Fit the socket and fix it with the solder melted.
At this time, do so while pressing with tweezers or fingers so that the socket will not float.

![17](https://user-images.githubusercontent.com/736191/46775631-0b3f4980-cd43-11e8-9542-1cc8677782dd.JPG)

Soldering is now complete.
When attaching an LED as an option, refer to the "LED" chapter below (it can be attached even after mounting a socket).

![18](https://user-images.githubusercontent.com/736191/46775632-0b3f4980-cd43-11e8-89a2-dda788a3e35b.JPG)

### Plate, switch

First insert the switch in the top plate.
Even afterwards, it is easier to put it in earlier, as it is necessary to put a little bit of challenge into the switch's fit.

![20](https://user-images.githubusercontent.com/736191/46775633-0bd7e000-cd43-11e8-9dc8-f66a0c14a258.JPG)

Finally, attach the spacer with screws so that the top plate, the PCB, the bottom plate are in order, and finish installing the cushion rubber at the four corners.

![21](https://user-images.githubusercontent.com/736191/46775634-0bd7e000-cd43-11e8-9523-54ebc370aa37.JPG)

## Firmware
https://docs.qmk.fm/#/newbs_getting_started Please refer to here and prepare the environment to write the firmware.

Once you have the environment, build the firmware for Crkbd with the following command.

```
make crkbd:default
```

When the build is completed, execute the following command.

```
make crkbd:default:avrdude
```

I think that it will be able to confirm that `.` Increases as the following logs are executed.
In the meantime press the reset switch ** twice ** to complete the firmware writing.

```
<省略>

Checking file size of crkbd_rev1_default.hex                                                        [OK]
 * File size is fine - 27328/28672
Copying crkbd_rev1_default.hex to qmk_firmware folder                                               [OK]
Detecting USB port, reset your controller now........
```

<When firmware writing to the ProMicro on one side is completed, the other will also write in the same procedure. Omission>

That is it.

## LED (optional)
We will install SK6812 MINI.

SK6812 MINI is very sensitive to heat, easily broken.
We recommend using a soldering iron with a temperature control function and working at temperatures around 220 ° C to 270 ° C.
Also, even if the temperature is adjusted, it will be damaged if the iron is applied to the LED for a long time, so we will try to solder as quickly as possible.
We will solder four LEDs at a time, but do not do 4 at a time, if you go two and prevent the rise in temperature of the LED, it will be hard to break, so it is recommended.

First of all it is confirmation of the installation position.

1 ~ 6 So that the backside (Undergrow) glows、7 ~ 27 Solder as the front side (Backlight) shines. Below is the position to attach the LED.

![23](https://user-images.githubusercontent.com/736191/46822561-c6f58d00-cdc6-11e8-90d4-de015410a7a4.png)
![24](https://user-images.githubusercontent.com/736191/46822569-cc52d780-cdc6-11e8-9602-f6265a2c876d.png)

1 ~ 6When soldering the black part enclosed with a circle as shown below, solder it so that the mark of the silk indicated by the arrow is on the top.
Please note that the direction changes with 1 to 3 and 4 to 5.

![26](https://user-images.githubusercontent.com/736191/46822428-6d8d5e00-cdc6-11e8-8858-06e8dbdb8ee8.png)

As shown below, solder 7-27 so that the largest pad surrounded by a circle and the silk mark indicated by the arrow are next to each other.

![30](https://user-images.githubusercontent.com/736191/46822434-6ebe8b00-cdc6-11e8-9686-69ac88bb4389.png)

If all soldering can be done normally it will shine as follows.
If there is only halfway lighting, LEDs are connected in the order of the number, so please doubt the soldering mistake of the LED that does not light or the LED before it or the damage of the LED.

![31](https://user-images.githubusercontent.com/736191/46822435-6ebe8b00-cdc6-11e8-892b-dc785fede9ea.JPG)

This is completed.

![32](https://user-images.githubusercontent.com/736191/46822437-6ebe8b00-cdc6-11e8-8754-aa3438a2eb7b.JPG)

