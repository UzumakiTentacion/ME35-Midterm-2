# ME35-Midterm-2
My ME35 Midterm 2 crazy thermostat code
Reads the temperature from the termistor, sends to airtable and an adafruit dashboard

Goal:

A crazy temperature monitor - individual project (help from TAs and me)

Design a temperature sensor that has:

1. A physical output of the temperature (could be a screen, LEDs, a motor-controlled pointer, etc connected to your Pico)
2. Pushes the temperature reading to an Adafruit dashboard every 5 min USING their MQTT broker
3. Integrates one i2c device in some way (completely your choice)
4. Changes from F to C depending on what color you hold in front of your computer camera
    1. Note that you will need to write a Python code on the PC (Mu or Thonny or…) that uses reads the airtable cell and uses MQTT to update your Adafruit dashboard.
    2. Your Pico should also read the airtable cell with RestAPI and change something on your display accordingly. The Pico should also update Adafruit with the latest reading.
    3. You have PyScript identify the color of the biggest blob in the image (is ir red, green, or blue - or you can play with harder colors like purple if you want) I would recommend using [thisLinks to an external site.](https://chrisrogers.pyscriptapps.com/me35-midterm/latest/) page. Remember to save your python you put in the REPL (if you want, you can clone your own version of the page and edit the HTML or the python).
    4. When your the code on your machine, it should take the snapped image, find the color and send it to [AirtableLinks to an external site.](https://www.airtable.com/) (you will have to create a free account, make a database, and then figure out their API - check [hereLinks to an external site.](https://airtable.com/developers/web/api/introduction) for help - if you scroll down, you can see a list of your databases - click on it and it will show you everything you need to get the API going - you do not even need their python library - do not forget to go [hereLinks to an external site.](https://airtable.com/create/tokens) to get an access token)
    5. A python program on your computer and Pico should then read the airtable entry and the PC should send it over MQTT to Adafruit.
