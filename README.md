# rainmachine-ipma
Instituto Português do Mar e da Atmosfera parser for the RainMachine sprinkler controller.

This parser was created to get local forecasts in Portugal from the Instituto Português do Mar e da Atmosfera (IPMA).  This parser uses the IPMA API available at [https://api.ipma.pt/](https://api.ipma.pt/).

## Setup
1. Download the file [ipma-parser.py](https://raw.githubusercontent.com/pjpeartree/rainmachine-ipma/master/ipma-parser.py)
2. Open the RainMachine Web Application https://xxx.xxx.xxx.xxx:8081/ui using your RainMachine IP address.
3. Login to your RainMachine device and then go to "Settings" - "Weather".
4. Click on "ADD NEW" button from the "Weather Services" section
5. Click on "Choose file" button and look for [ipma-parser.py](https://raw.githubusercontent.com/pjpeartree/rainmachine-ipma/master/ipma-parser.py) file on your computer.
6. Click "UPLOAD" to add the new weather data source parser.
7. After successfully uploaded the new parser will be listed under "User uploaded" tab from the "Weather Services" section.
8. Click on it and check the "Enable" option to activate the parser
9. Click on "REFRESH NOW" button to fetch the weather data for the first time.

You do not need to configure any parameter. The parser will auto-discover the nearst IPMA Station available in less that 10 km.

## Known Installation Issues
* You might encounter an issue if the [ipma-parser.py](https://raw.githubusercontent.com/pjpeartree/rainmachine-ipma/master/ipma-parser.py) file size is too big when using the remote access service (https://my.rainmachine.com) to upload the parser and it's preferable to use the direct local connection by just going to RainMachine IP address.
 
### Forecast Data
The parser runs every 3600 seconds and adds the following data:

* TEMPERATURE
* MINTEMP
* MAXTEMP
* RH
* WIND
* POP
* CONDITION

## Authors

* **Pedro J. Pereira** - *Initial work* - [pjpeartree](https://github.com/pjpeartree)


## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE.md](LICENSE.md) file for details
