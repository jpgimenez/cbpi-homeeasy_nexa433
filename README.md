# cbpi-homeeasy_nexa433
Plugin for CraftBeerPi for HomeEasy and Nexa 433 mhz self-learning power sockets. Interim solution to enable the use of Nexa/Homeeasy 433 mhz sockets. 
<br>
## HARDWARE PREREQUISITES:
- Self learning Nexa/HomeEasy 433 mhz power socket (tested with Nexa PE-3 och Nexa MYCR-3)
- Rf 433 mhz transmitter, e.g. FS1000A (2-3 USD on Ebay)

## SOFTWARE INSTALLATION:
### 1. Install piHomeEasy (https://github.com/nbogojevic/piHomeEasy)

#### Install WiringPi
```bash
cd ~
sudo apt-get install git-core
git clone git://git.drogon.net/wiringPi
cd wiringPi
sudo ./build
```
#### Install piHomeEasy
```bash
cd ~
git clone git://github.com/nbogojevic/piHomeEasy
cd piHomeEasy
sudo make install
```

### 2. Install the plugin
- Install repository
```bash
cd ~/craftbeerpi3/modules/plugins/
git://github.com/Lai1337/cbpi-homeeasy_nexa433
```
or put the file `__init__.py` in a new folder in `craftbeerpi3/modules/plugins/`
<br>
- Create 2 files in `/home/pi`: 
`actor-on.sh` and `actor-off.sh` (see examples in repository)

## USAGE
- Connect Rf transmitter has 3 pins: VCC, GND och DATA
Default is to connect DATA to GPIO 17 (Pin 0 i WiringPi)
![alt text](https://github.com/Lai1337/cbpi-homeeasy_nexa433/blob/master/Wiring.png)
- Pair power socket EXAMPLE `piHomeEasy 0 56123 1 on`
