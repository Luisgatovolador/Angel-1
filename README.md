[flows.json](https://github.com/Ale0515-GG/Angel/files/13572076/flows.json)# Angel

# Personaje Navideno

##Nombre del personaje

-Nombre de tu personaje
-Angel
##Integrantes
- Mayra Alejandra Galvan Garcia
- Luis Oswaldo Rodriguez Lopez

## Materiales a utilizar

|Nombre del componente|Descripcion|Cantidad|Precio|
|-|-|-|-|
|ESP32|Microcontrolador con 30 pines con comunicacion Wifi y Bluetooth|1|$140.00|
|Cables dupont|Cables para conexion de prototipos de pruebas|50|$60.00|
|Servos|Es un control preciso de la posición y movimiento gracias a su motor, engranajes y retroalimentación|2|$100.00|
|Buzzer|Emite sonidos y tonos mediante vibraciones controladas eléctricamente.|1|$60.00|
|Led|Emiten luz cuando se aplica corriente|30|$80.00|
|Resistor|Protegen los LEDs al limitar la corriente. Garantizan un funcionamiento seguro y prolongado al ajustar la resistencia eléctrica. Indispensables al conectar LEDs a una fuente de alimentación.|30|$70.00|

Complementa la tabla
##software a utilizar
| Nombre | Version | Tipo software |
|-|-|-|
| Thonny | 4.2.1 | Software Libre |
| SSD1602 | 1.8.1 | Software Libre |
| hcsr04 | libreria | Software Libre |
| ssd1306 | Libreria | Software Libre |

## Prototipo en dibujo
- Fotofragia de dibujo a mano alzada de tu personaje
![WhatsApp Image 2023-11-09 at 21 47 42](https://github.com/Ale0515-GG/Angel/assets/116208731/d7e2c8d1-2b71-403b-818e-f0f70606bcec)



## Comunicacion
- Describir la manera que creen que utilizaria su celular para comunicarse con su personaje

- Desde el celular se podra escoger el color de las luces de el Angel ademas de la musica que estara sonando desde el Angel

## Arquitectura
-Diagrama que contenga los sensores, los actuadores, el microcontrolador, el servidor.
![image](https://github.com/Ale0515-GG/Angel/assets/116208731/4e00b3db-4a59-461f-afdb-782ad32fad22)
![WhatsApp Image 2023-11-09 at 20 58 17](https://github.com/Ale0515-GG/Angel/assets/116208731/cece174d-841c-418e-a8c0-6c537a9f0381)


## Base de Datos
-Imagen tabla o tablas que usarias (Ej. sensores, actuadores, modelo relacional)

![image](https://github.com/Ale0515-GG/Angel/assets/116208731/c893a0c4-39ae-4e6c-be09-20eb2ad24e83)

## Video


## Flujo
[U[
    {
        "id": "bf8d702680590f54",
        "type": "tab",
        "label": "Flow 1",
        "disabled": false,
        "info": "",
        "env": []
    },
    {
        "id": "83fd9c7c4903b2db",
        "type": "ui_switch",
        "z": "bf8d702680590f54",
        "name": "",
        "label": "Luces",
        "tooltip": "",
        "group": "1e1513d916ed20a6",
        "order": 0,
        "width": 0,
        "height": 0,
        "passthru": true,
        "decouple": "false",
        "topic": "topic",
        "topicType": "msg",
        "style": "",
        "onvalue": "1",
        "onvalueType": "num",
        "onicon": "",
        "oncolor": "",
        "offvalue": "0",
        "offvalueType": "num",
        "officon": "",
        "offcolor": "",
        "animate": false,
        "className": "",
        "x": 470,
        "y": 260,
        "wires": [
            [
                "42060d1bf082779e"
            ]
        ]
    },
    {
        "id": "218639955cf7630a",
        "type": "inject",
        "z": "bf8d702680590f54",
        "name": "Inicio",
        "props": [
            {
                "p": "payload"
            },
            {
                "p": "topic",
                "vt": "str"
            }
        ],
        "repeat": "",
        "crontab": "",
        "once": true,
        "onceDelay": 0.1,
        "topic": "",
        "payload": "",
        "payloadType": "str",
        "x": 290,
        "y": 300,
        "wires": [
            [
                "83fd9c7c4903b2db",
                "5025d4e6a047b752"
            ]
        ]
    },
    {
        "id": "42060d1bf082779e",
        "type": "mqtt out",
        "z": "bf8d702680590f54",
        "name": "",
        "topic": "utng/lorl/led",
        "qos": "",
        "retain": "",
        "respTopic": "",
        "contentType": "",
        "userProps": "",
        "correl": "",
        "expiry": "",
        "broker": "74502b89fef40f66",
        "x": 670,
        "y": 300,
        "wires": []
    },
    {
        "id": "5025d4e6a047b752",
        "type": "ui_switch",
        "z": "bf8d702680590f54",
        "name": "",
        "label": "Canciones",
        "tooltip": "",
        "group": "778f3338e8d74b8f",
        "order": 0,
        "width": 0,
        "height": 0,
        "passthru": true,
        "decouple": "false",
        "topic": "topic",
        "topicType": "msg",
        "style": "",
        "onvalue": "4",
        "onvalueType": "num",
        "onicon": "",
        "oncolor": "",
        "offvalue": "3",
        "offvalueType": "num",
        "officon": "",
        "offcolor": "",
        "animate": false,
        "className": "",
        "x": 490,
        "y": 320,
        "wires": [
            [
                "42060d1bf082779e"
            ]
        ]
    },
    {
        "id": "52fd9f3bdcf97c04",
        "type": "remote-access",
        "z": "bf8d702680590f54",
        "confignode": "6cc609285e090632",
        "name": "",
        "verbose": 0,
        "x": 440,
        "y": 460,
        "wires": [
            [],
            []
        ]
    },
    {
        "id": "1e1513d916ed20a6",
        "type": "ui_group",
        "name": "Group 1",
        "tab": "ea5db9f4b6d3e11a",
        "order": 1,
        "disp": true,
        "width": "6",
        "collapse": false,
        "className": ""
    },
    {
        "id": "74502b89fef40f66",
        "type": "mqtt-broker",
        "name": "",
        "broker": "broker.emqx.io",
        "port": "1883",
        "clientid": "",
        "autoConnect": true,
        "usetls": false,
        "protocolVersion": "4",
        "keepalive": "60",
        "cleansession": true,
        "autoUnsubscribe": true,
        "birthTopic": "",
        "birthQos": "2",
        "birthRetain": "false",
        "birthPayload": "",
        "birthMsg": {},
        "closeTopic": "",
        "closeQos": "0",
        "closeRetain": "false",
        "closePayload": "",
        "closeMsg": {},
        "willTopic": "",
        "willQos": "0",
        "willRetain": "false",
        "willPayload": "",
        "willMsg": {},
        "userProps": "",
        "sessionExpiry": ""
    },
    {
        "id": "778f3338e8d74b8f",
        "type": "ui_group",
        "name": "Group 2",
        "tab": "ea5db9f4b6d3e11a",
        "order": 2,
        "disp": true,
        "width": "6",
        "collapse": false,
        "className": ""
    },
    {
        "id": "6cc609285e090632",
        "type": "remote-config",
        "name": "Node-RED UI",
        "host": "localhost",
        "protocol": "http",
        "port": "1880",
        "baseurl": "/ui",
        "instancehash": "uing3h17jgtq13300mxm6h8mtjkq3vok7i4pxw041zv3b7zq48ldi3amru5vamvr",
        "server": "nodered02.remote-red.com",
        "region": "de"
    },
    {
        "id": "ea5db9f4b6d3e11a",
        "type": "ui_tab",
        "name": "Tab 2",
        "icon": "dashboard",
        "order": 2
    }
]ploading flows.json…]()

