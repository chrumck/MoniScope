## MoniScope

### So, this is the beginning...

**MoniScope** is going to be a web application which will work pretty much like Google Maps... except for measurements. The aim is to build a crisp, intuitive interface to show measurements from variety of wireless remote sensors, be it simple temperature gauge in your basement, a voltage and speed sensor in your car, or a complex network of instruments on a construction site to measure the influence of site activities on the surroundings. 

The idea is to make it work hassle free. I mean, really hassle free. You just get the instrument (build it yourself with the instructions available here, or let me help you build one), switch it on, give it credentials to talk to MoniScope, and the rest is magic. From this moment on, you can see the sensor on the map based on its GPS location, view the readings and check its status. You don't like what you see out of the box? Tweak things right from MoniScope. Change reading interval to save power, move its position, set alert levels, group it with other sensors - the list goes on here. As long as the instrument gets power, you will be able to do the rest from your couch!

### The instruments 

[Here is an example of the hardware which I will use with **MoniScope**](https://www.sierrawireless.com/products-and-solutions/routers-gateways/rv50/), Raven RV50

![Sierra Wireless Raven RV50](https://www.sierrawireless.com/-/media/iot/products/gatewayproductpages/gateways_rv50_475x274.png?la=en)

[I will use its LUA based application framework](http://source.sierrawireless.com/resources/airlink/aleos_af/refdoc_aleos_af_api_1_3/) to make it do whatever I want. For starters, I'm going to mount it in my motorcycle to measure battery voltage, bike's speed.

### So, this is the idea... Let's see where it leads me.

## And remember, this is all to FS!

