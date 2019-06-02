[This file also exists in ENGLISH](readme_ENG.md)

# ESP8266 MicroPython Driver

Voici une collection de pilote (et raccordements) pour différents breakouts utilisés avec un __ESP8266 reflashé en MicroPython__.

SI cela fonctionne sous ESP8266 ALORS cela fonctionnera aussi sur la [MicroPython Pyboard](https://shop.mchobby.be/fr/56-micropython) et tout autre carte MicroPython!

La plateforme la plus facile à flasher est un [Feather ESP8266 HUZZA ADA2821](http://shop.mchobby.be/product.php?id_product=846) ou une [carte d'évaluation ESP8266-EVB d'Olimex](https://shop.mchobby.be/esp8266-esp32-wifi-iot/668-module-wifi-esp8266-carte-d-evaluation-3232100006683-olimex.html) ou les [cartes WEMOS / LOLIN (modules ESP)](https://shop.mchobby.be/fr/123-wemos-lolin-esp)

![ESP8266 et Pyboard](docs/_static/ESP8266-to-PYBOARD.jpg)
![Feather ESP8266](docs/_static/FEAT-HUZZA-ESP8266-01.jpg)
![Olimex ESP8266 Evaluation Board](docs/_static/ESP8266-EVB.jpg)
![Wemos D1 (ESP8266)](docs/_static/WEMOS-D1.jpg)

# Autres sources d'information
* [__Wiki pour MicroPython sur ESP8266__]( https://wiki.mchobby.be/index.php?title=MicroPython-Accueil#ESP8266_en_MicroPython) pour apprendre comment flasher votre ESP sous MicroPython.
* [__GitHub dédicacé Pyboard__](https://github.com/mchobby/pyboard-driver) avec des pilotes nécessitant plus de ressources. https://github.com/mchobby/pyboard-driver.
* Achat de matériel - https://shop.mchobby.be

# Bibliothèques disponibles
Voici une description des bibliothèques disponibles dans ce dépôt. <strong>Chaque sous-répertoire contient des instructions, schémas et codes dans un readme.md personnalisé.</strong>


Explorer par:
* Interface:
[FEATHERWING](docs/drv_by_intf_FEATHERWING.md), [GPIO](docs/drv_by_intf_GPIO.md), [I2C](docs/drv_by_intf_I2C.md), [NCD](docs/drv_by_intf_NCD.md), [ONEWIRE](docs/drv_by_intf_ONEWIRE.md), [QWIIC](docs/drv_by_intf_QWIIC.md), [SPI](docs/drv_by_intf_SPI.md), [UART](docs/drv_by_intf_UART.md), [UEXT](docs/drv_by_intf_UEXT.md)
* Fabriquant:
[ADAFRUIT](docs/drv_by_man_ADAFRUIT.md), [NCD](docs/drv_by_man_NCD.md), [NONE](docs/drv_by_man_NONE.md), [OLIMEX](docs/drv_by_man_OLIMEX.md), [SPARKFUN](docs/drv_by_man_SPARKFUN.md)

<table>
<thead>
  <th>Répertoire</th><th>Description</th>
</thead>
<tbody>
  <tr><td>NCD</td>
      <td><strong>Composants</strong> : NCD<br />
      <strong>Interfaces</strong> : I2C, NCD<br />
      <strong>Testé avec</strong> : ESP8266-EVB, FEATHER-ESP8266, WEMOS-D1<br />
<small>Connecter facilement une __mini carte I2C__ de NCD (National Control Device) sur une carte MicroPython grâce au connecteur <strong>NCD</strong> qui facilite grandement les raccordements de périphérique I2C. Logique 5V.</small>
<br /><ul>
<li>Voir <a href="https://ncd.io/">NCD.io</a></li>
<li>Voir <a href="https://ncd.io/">National Control Device</a></li>
</ul>
      </td>
  </tr>
  <tr><td>UEXT</td>
      <td><strong>Composants</strong> : UEXT<br />
      <strong>Interfaces</strong> : I2C, SPI, UART<br />
      <strong>Testé avec</strong> : ESP8266-EVB<br />
<small>Connecteur <strong>UEXT</strong> en logique 3.3V est utilisé sur les cartes et capteurs d' Olimex. Il transporte les bus I2C, SPI, UART et alimentation 3.3V</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/fr/138-uext">UEXT @ MCHobby</a></li>
<li>Voir <a href="https://www.olimex.com/Products/Modules/">UEXT @ Olimex</a></li>
</ul>
      </td>
  </tr>
  <tr><td>ads1015-ads1115</td>
      <td><strong>Composants</strong> : ADS1015, ADS1115, ADA1085<br />
      <strong>Interfaces</strong> : I2C<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266<br />
<small>Convertisseur ADC (Analogique vers Digital) 4 canaux pour réaliser des lectures analogiques et lectures différentielles.<br />L'ADS1115 dispose d'un amplificateur interne programmable, ce qui permet de lire des tensions très faibles.</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/breakout/362-ads1115-convertisseur-adc-16bits-i2c-3232100003620-adafruit.html">ADS1115 breakout</a></li>
</ul>
      </td>
  </tr>
  <tr><td>am2315</td>
      <td><strong>Composants</strong> : AM2315<br />
      <strong>Interfaces</strong> : I2C<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266<br />
<small>Capteur de <strong>température et humidité</strong> relative (0 à 100%) pour relevés en extérieur.</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/fr/environnemental-press-temp-hrel-gaz/932-am2315-senseur-de-temperature-et-humidite-sous-boitier-3232100009325.html">AM2315 Sensor</a></li>
</ul>
      </td>
  </tr>
  <tr><td>bme280-bmp280</td>
      <td><strong>Composants</strong> : BME280, BMP280, ADA2651, ADA2652<br />
      <strong>Interfaces</strong> : I2C<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266<br />
<small>Le BMP280 est un senseur de <strong>pression et température</strong> très populaire.<br />Le BME280 est un senseur de <strong>pression, température et HUMIDITÉ</strong> relative</small>
<br /><ul>
<li>Voir <a href="http://shop.mchobby.be/product.php?id_product=1118">BMP280 Sensor</a></li>
<li>Voir <a href="http://shop.mchobby.be/product.php?id_product=684">BME280 Sensor</a></li>
</ul>
      </td>
  </tr>
  <tr><td>bmp180</td>
      <td><strong>Composants</strong> : BMP180<br />
      <strong>Interfaces</strong> : I2C<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266<br />
<small>Le BMP180 est un senseur de <strong>pression et température</strong> aujourd'hui remplacé par le BMP280.</small>
<br /><ul>
<li>Voir <a href="http://shop.mchobby.be/product.php?id_product=397">BMP180 Sensor</a></li>
</ul>
      </td>
  </tr>
  <tr><td>dht11</td>
      <td><strong>Composants</strong> : DHT11<br />
      <strong>Interfaces</strong> : GPIO<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266<br />
<small>Le DHT11 est un senseur d'<strong>humidité</strong> (20 à 80%) et température très bon marché.</small>
<br /><ul>
<li>Voir <a href="http://shop.mchobby.be/product.php?id_product=708">DHT11 Sensor</a></li>
</ul>
      </td>
  </tr>
  <tr><td>ds18b20</td>
      <td><strong>Composants</strong> : DS18B20<br />
      <strong>Interfaces</strong> : ONEWIRE<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266<br />
<small>Le DS18B20 est un senseur de <strong>température</strong> digital très populaire. Il utilise le bus 1-Wire permettant de brancher plusieurs senseurs 1-Wire sur un même bus.</small>
<br /><ul>
<li>Voir <a href="http://shop.mchobby.be/product.php?id_product=259">DS18B20 Sensor</a></li>
</ul>
      </td>
  </tr>
  <tr><td>mcp230xx</td>
      <td><strong>Composants</strong> : MCP23017, MCP23008<br />
      <strong>Interfaces</strong> : I2C<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266<br />
<small>Le MCP23017 (et MCP2308) sont des <strong>GPIO Expander</strong> permettant d'ajouter des entrées/sorties supplémentaires sur un microcontrôleur.</small>
<br /><ul>
<li>Voir <a href="http://shop.mchobby.be/product.php?id_product=218">MCP23017 GPIO Expander</a></li>
</ul>
      </td>
  </tr>
  <tr><td>modio</td>
      <td><strong>Composants</strong> : MOD-IO<br />
      <strong>Interfaces</strong> : I2C, UEXT<br />
      <strong>Testé avec</strong> : ESP8266-EVB<br />
<small>MOD-IO est une carte d'extension I2C avec port de connexion <strong>UEXT</strong>. Cette carte d'Olimex équipé de relais, d'entrée OptoCoupleur (24V) et entrées analogiques (0-3.3V).<br />Cette carte est compatible avec le standard industriel en 24V.</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/fr/138-uext">UEXT @ MCHobby</a></li>
<li>Voir <a href="https://www.olimex.com/Products/Modules/">UEXT @ Olimex</a></li>
</ul>
      </td>
  </tr>
  <tr><td>modio2</td>
      <td><strong>Composants</strong> : MOD-IO2<br />
      <strong>Interfaces</strong> : I2C, UEXT<br />
      <strong>Testé avec</strong> : ESP8266-EVB<br />
<small>MOD-IO est une carte d'extension I2C avec port de connexion <strong>UEXT</strong>. Cette carte d'Olimex équipé de relais, de GPIO aux fonctions multiples (Input, Output, Analog, PWM; 0-3.3V).</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/fr/138-uext">UEXT @ MCHobby</a></li>
<li>Voir <a href="https://www.olimex.com/Products/Modules/">UEXT @ Olimex</a></li>
</ul>
      </td>
  </tr>
  <tr><td>modlcd1x9</td>
      <td><strong>Composants</strong> : MOD-LCD-1x9<br />
      <strong>Interfaces</strong> : I2C, UEXT<br />
      <strong>Testé avec</strong> : ESP8266-EVB<br />
<small>MOD-LCD1x9 est un afficheur 9 caractères alphanumérique I2C avec port de connexion <strong>UEXT</strong>.</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/esp8266-esp32-wifi-iot/1414-uext-lcd-display-1-line-of-9-alphanumeric-chars-3232100014145-olimex.html">MOD-LCD1x9 @ MCHobby</a></li>
<li>Voir <a href="https://www.olimex.com/Products/Modules/">UEXT @ Olimex</a></li>
</ul>
      </td>
  </tr>
  <tr><td>modltr501</td>
      <td><strong>Composants</strong> : MOD-LTR-501ALS, LTR-501ALS<br />
      <strong>Interfaces</strong> : I2C, UEXT<br />
      <strong>Testé avec</strong> : ESP8266-EVB<br />
<small>LTR-501ALS permet de faire une lecture de luminosité de 0.01 à 64.000 Lux (64K lux) et détection de proximité (jusqu'à 10cm). Le MOD-LTR-501ALS dispose d'une connexion <strong>UEXT</strong> facilitant les raccordements.</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/uext/1415-senseur-proximite-et-lumiere-ltr501-connecteur-uext-3232100014152-olimex.html">MOD-LTR-501ALS @ MCHobby</a></li>
<li>Voir <a href="https://www.olimex.com/Products/Modules/">UEXT @ Olimex</a></li>
</ul>
      </td>
  </tr>
  <tr><td>modmag</td>
      <td><strong>Composants</strong> : MOD-MAG, MAG3110<br />
      <strong>Interfaces</strong> : I2C, UEXT<br />
      <strong>Testé avec</strong> : ESP8266-EVB<br />
<small>Le MAG3110 est un magénomètre digital 3 axes de NXP accessible via I2C. Le MOD-MAG dispose d'une connexion <strong>UEXT</strong> facilitant les raccordements.</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/esp8266-esp32-wifi-iot/1413-uext-mag3110-magnetometer-module-3232100014138-olimex.html">MOD-MAG @ MCHobby</a></li>
<li>Voir <a href="https://www.olimex.com/Products/Modules/">UEXT @ Olimex</a></li>
</ul>
      </td>
  </tr>
  <tr><td>modoled128x64</td>
      <td><strong>Composants</strong> : SSD1306, MOD-OLED-128x64, OLED<br />
      <strong>Interfaces</strong> : I2C, UEXT<br />
      <strong>Testé avec</strong> : ESP8266-EVB<br />
<small>Un afficheur OLED 128x64 avec contrôleur SSD1306 (I2C) et connecteur UEXT.</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/product.php?id_product=1411">Afficheur OLED 128 x 64 avec interface I2C et UEXT</a></li>
</ul>
      </td>
  </tr>
  <tr><td>modrgb</td>
      <td><strong>Composants</strong> : MOD-RGB<br />
      <strong>Interfaces</strong> : I2C, UEXT<br />
      <strong>Testé avec</strong> : ESP8266-EVB<br />
<small>MOD-RGB est une carte d'extension I2C avec port de connexion <strong>UEXT</strong>. Cette carte d'Olimex équipé de MosFet de puissance pour commander des rubans LED RGB analogiques via I2C (ou DMX).</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/fr/138-uext">UEXT @ MCHobby</a></li>
<li>Voir <a href="https://www.olimex.com/Products/Modules/">UEXT @ Olimex</a></li>
</ul>
      </td>
  </tr>
  <tr><td>modwii</td>
      <td><strong>Composants</strong> : MOD-Wii-UEXT-NUNCHUCK, NUNCHUCK<br />
      <strong>Interfaces</strong> : I2C, UEXT<br />
      <strong>Testé avec</strong> : ESP8266-EVB<br />
<small>La Wii NUNCHUCK est une manette de jeu super confortable et s'utilise sur le bus I2C. Ce controleur dispose d'une connexion <strong>UEXT</strong> facilitant les raccordements.</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/esp8266-esp32-wifi-iot/1416-uext-wii-nunchuck-controller-3232100014169-olimex.html">Wii Nunchuck game controller (UEXT) @ MCHobby</a></li>
<li>Voir <a href="https://www.olimex.com/Products/Modules/">UEXT @ Olimex</a></li>
</ul>
      </td>
  </tr>
  <tr><td>ncd-fet-solenoid</td>
      <td><strong>Composants</strong> : I2CDRV8W4I12V, MCP23008<br />
      <strong>Interfaces</strong> : I2C, NCD<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266, PYBOARD<br />
<small>Contrôleur de sortie FET + GPIO (basé sur un MCP23008) pour charge résistive / inductive 12V (valve). La <i>carte I2C de NCD</i> propose un  connecteur <strong>NCD</strong> qui facilite grandement les raccordements de périphérique I2C.<br />Ce senseur est également disponible sous forme de breakout.</small>
<br /><ul>
<li>Voir <a href="https://ncd.io/">NCD.io</a></li>
<li>Voir <a href="https://ncd.io/">National Control Device</a></li>
</ul>
      </td>
  </tr>
  <tr><td>ncd-mpl115A2</td>
      <td><strong>Composants</strong> : MPL115A2, ADA992<br />
      <strong>Interfaces</strong> : I2C, NCD<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266, PYBOARD<br />
<small>Le MPL115A2 est un capteur de pression et température I2C. La <i>mini carte I2C de NCD</i> propose un  connecteur <strong>NCD</strong> qui facilite grandement les raccordements de périphérique I2C.<br />Ce senseur est également disponible sous forme de breakout.</small>
<br /><ul>
<li>Voir <a href="https://ncd.io/">NCD.io</a></li>
<li>Voir <a href="https://ncd.io/">National Control Device</a></li>
</ul>
      </td>
  </tr>
  <tr><td>ncd-oled</td>
      <td><strong>Composants</strong> : SSD1306, I2COLED, OLED<br />
      <strong>Interfaces</strong> : I2C, NCD<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266, PYBOARD<br />
<small>Un afficheur OLED 128x64 avec contrôleur SSD1306 (I2C) et connecteur NCD.</small>
<br /><ul>
<li>Voir <a href="https://ncd.io/">NCD.io - National Control Device</a></li>
<li>Voir <a href="https://store.ncd.io/product/oled-128x64-graphic-display-i2c-mini-module/">NCD oled 128x64 i2c mini module</a></li>
</ul>
      </td>
  </tr>
  <tr><td>ncd-pecmac</td>
      <td><strong>Composants</strong> : DLCT27C10, OPCT16AL, I2CCMAC230A, PECMAC2xxxA<br />
      <strong>Interfaces</strong> : I2C, NCD<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266, PYBOARD<br />
<small>Capteur de courant alternatif sur bus I2C (ou interface IoT). La <i>carte I2C de NCD</i> propose un  connecteur <strong>NCD</strong> qui facilite grandement les raccordements de périphérique I2C.<br />Ce senseur est également disponible sous forme de breakout.</small>
<br /><ul>
<li>Voir <a href="https://ncd.io/">NCD.io</a></li>
<li>Voir <a href="https://ncd.io/">National Control Device</a></li>
</ul>
      </td>
  </tr>
  <tr><td>ncd-si7005</td>
      <td><strong>Composants</strong> : SI7005<br />
      <strong>Interfaces</strong> : I2C, NCD<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266, PYBOARD<br />
<small>Le SI7005 est un capteur d'humidité relative et température I2C. La <i>mini carte I2C de NCD</i> propose un  connecteur <strong>NCD</strong> qui facilite grandement les raccordements de périphérique I2C.<br />Ce senseur est également disponible sous forme de breakout.</small>
<br /><ul>
<li>Voir <a href="https://ncd.io/">NCD.io</a></li>
<li>Voir <a href="https://ncd.io/">National Control Device</a></li>
</ul>
      </td>
  </tr>
  <tr><td>ncd-water-detect</td>
      <td><strong>Composants</strong> : WATER-DETECT, WDBZ, PCA9536<br />
      <strong>Interfaces</strong> : I2C, NCD<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266, PYBOARD<br />
<small>Détecteur de présence d'eau + Buzzer + 2 GPIOs (basé sur un PCA9536). La <i>mini carte I2C de NCD</i> propose un  connecteur <strong>NCD</strong> qui facilite grandement les raccordements de périphérique I2C.<br />Ce senseur est également disponible sous forme de breakout.</small>
<br /><ul>
<li>Voir <a href="https://ncd.io/">NCD.io</a></li>
<li>Voir <a href="https://ncd.io/">National Control Device</a></li>
</ul>
      </td>
  </tr>
  <tr><td>neopixel</td>
      <td><strong>Composants</strong> : NEOPIXEL, 74AHCT125<br />
      <strong>Interfaces</strong> : GPIO<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266<br />
<small>Les <strong>NéoPixels</strong> sont des LEDs digitales intelligentes pouvant être contrôlées indépendamment les unes des autres.</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/fr/55-neopixels-et-dotstar">NeoPixels</a></li>
<li>Voir <a href="https://shop.mchobby.be/fr/ci/1041-74ahct125-4x-level-shifter-3v-a-5v-3232100010413.html">74AHCT125</a></li>
</ul>
      </td>
  </tr>
  <tr><td>oled-ssd1306</td>
      <td><strong>Composants</strong> : SSD1306, FEATHER-OLED-WING, ADA2900, OLED<br />
      <strong>Interfaces</strong> : I2C, FEATHERWING<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266<br />
<small>Le SSD1306 est un contrôleur d'écran OLED</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/product.php?id_product=879">FeatherWing OLED ssd1306 128x32</a></li>
</ul>
      </td>
  </tr>
  <tr><td>pca9536</td>
      <td><strong>Composants</strong> : PCA9536<br />
      <strong>Interfaces</strong> : I2C<br />
      <strong>Testé avec</strong> : <br />
<small>Contrôleur GPIO 4 bits I2C.</small>
      </td>
  </tr>
  <tr><td>tsl2561</td>
      <td><strong>Composants</strong> : TSL2561, ADA439<br />
      <strong>Interfaces</strong> : I2C<br />
      <strong>Testé avec</strong> : FEATHER-ESP8266<br />
<small>Le TSL2561 est un senseur de <strong>luminosité</strong> en lumière visible ayant un réponse proche de l'oeil humain. Retourne une valeur en LUX</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/product.php?id_product=238">Capteur Lux/Luminosité/Lumière digital</a></li>
</ul>
      </td>
  </tr>
  <tr><td>umqtt</td>
      <td><strong>Composants</strong> : <br />
      <strong>Interfaces</strong> : <br />
      <strong>Testé avec</strong> : FEATHER-ESP8266, PYBOARD<br />
<small>Exemples de communication MQTT avec un module ESP8266.</small>
<br /><ul>
<li>Voir <a href="https://shop.mchobby.be/product.php?id_product=846">Feather ESP8266</a></li>
</ul>
      </td>
  </tr>
</tbody>
</table>

# Quelques ressources utiles
* [how-to-install-upy.md](how-to-install-upy.md) contient un résumé condensé pour une installation depuis Linux
 * [erase-esp8266.sh](erase-esp8266.sh) - A adapter. Permet d'effacer la flash de l'ESP8266
 * [burn-esp8266.sh](burn-esp8266.sh) - A adapter. Permet de flasher un [binaire téléchargé depuis micropython.org/download](https://micropython.org/download/) sur un ESP8266
* fichiers de configuration
 * [boot.py](boot.py) - A adapter avec l'identifiant et mot de passe de votre réseau WiFi. Une fois copié sur votre ESP8266 (avec RShell), celui-ci se connectera automatiquement sur votre réseau WiFi
 * [port_config.py](port_config.py) - A adapter. Placez y le mot de passe qui protégera votre connexion WebRepl. Une fois copié sur votre ESP8266 (avec REPL), il sera automatiquement utilisé par WebRepl.  

## RShell

__RShell__ est un outil formidable qui permet de d'éditer/transférer/repl sur une carte MicroPython a travers une simple connexion série (et même Bluetooth serial).

C'est un outil vraiment _très utile_ qui vaut la peine de s'y attarder... avec lui plus besoin d'avoir accès au "lecteur Flash" de votre carte MicroPython pour y éditer ou y copier un fichier.

Ce qu'il y de génial avec RShell, c'est qu'il fonctionne aussi avec ESP8266 (tant mieux parce qu'il n'y a pas de _lecteur flash_ comme sur une PyBoard).

 * [Tuto RShell en Français](https://wiki.mchobby.be/index.php?title=MicroPython-Hack-RShell)
 * [Github de rshell](https://github.com/dhylands/rshell) - documentation et instruction d'installation.
 * [rshell-esp8266.sh](rshell-esp8266.sh) - A adapater. Appel RShell avec buffer réduit pour ESP8266.

__ATTENTION__ : pour un ESP8266 il faut absolument réduire le buffer d'échange... sinon on écrase facilement le système de fichier (et il faudra reflasher la bête) :-/  Voyez le fichier [rshell-esp8266.sh](rshell-esp8266.sh) qui est proposé ici.

## WebRepl

![Repl](dht11/dht11_webrepl.jpg)

Ouvrez WebRepl.html dans votre navigateur et vous pourrez entamer une session REPL avec votre Feather ESP8266 au travers d'une session HTTP.

Tout ce que vous avez besoin de connaître, c'est soit son adresse IP, soit son nom sur le réseau.

__ATTENTION__ :
* Il convient d'avoir un fichier [boot.py](boot.py) correctement configuré pour que votre ESP8266 puisse se connecter sur votre réseau WiFi.
* Vous pouvez également pré-initialiser votre mot de passe WebRepl dans [port_config.py](port_config.py). Les versions plus récentes de MicroPython place le mot de passe dans le fichier boot.py.
RShell sera un outil précieux pour vous assister dans cette tâche.

# Feather ESP8266 Huzza, bus I2C, bloc d'alim. et boot qui plante

Suite à de nombreux tests, nous avons remarqués que l'utilisation de la broche 5 (SCL) sur le Feather ESP8266 Huzza provoquait parfois des problèmes de démarrage dans certains cas. [Voyez ce billet](https://forums.adafruit.com/viewtopic.php?f=57&t=105635)

En effet l'utilisation d'un _bloc d'alimentation_ micro-USB (donc sans USB-Série) _empêche le Feather ESP8266 de booter si un périphérique I2C_ est branché sur SCL (pin 5). En l’occurrence, il s'agissait un senseur Humidité + Température AM2315 (_utilisé seul sur le bus I2C en Pin 4 et 5_).

Avec le temps et nombreuses autres situations, nous avons fini par remarquer que l'AM2315 n'embarque pas de résistance pull-up sur les lignes SDA et SCL.

Si vous rencontrez cette situation, il y a deux solutions:
* Utiliser la broche 2 comme signal SCL pour votre bus I2C (en guise de test par exemple).
* Vérifier s'il manque des résistances pull-up sur le senseur (à coup sûr pour l'AM2315) et les ajouter vous même.

# Lien divers

Il y a de nombreux pilotes Adafruit sur ce Github (Tony Dicola)
* https://github.com/adafruit/micropython-adafruit-bundle/tree/master/libraries/drivers

Également trouvé des pilotes pour centrales Intertielles sur ce Github
* https://github.com/micropython-IMU/
