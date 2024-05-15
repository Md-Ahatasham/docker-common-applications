## JetBrainCredentials ##
username: brainchildsoft@gmail.com
password: <?KnightC0der?>
##


**Load Testing**

Jmeter installation requirement

     . JDK 8+
          . sudo apt install default-jre (This will install the latest JDK, right now JDK-11)
          . check jdk version (java --version)

     . Download Jmeter use this link -> https://jmeter.apache.org/download_jmeter.cgi
          . choose second option under binaries tab (apache-jmeter-5.6.2.zip	sha512 pgp)
          . unzip apache-jmeter-5.6.2.zip
          . Go to bin folder and run this command to open jmeter through terminal (./jmeter)

     . Configuration
          . install plugin manager from this link (https://jmeter-plugins.org/install/Install/)
          . keep this file within (lib/ext) folder and restart jmeter
          . we will find new option within options tab named plugin manager
          . after clicking on plugin manager from available plugin select (throughput shaping timer plugin)
   

     . Load test instruction
          . First open jmeter we will find there is a default plan in sidebar called " Test Plan"
          . Right click on "Test Plan" Then click on "add->Threads (Users) ->Thread Group"
          . You will see another menu under "Test Plan" named "Thread Group"
          . Click on "Thread Group" we will find some configuration in right side
          . From there we have to configure some options like ->
               . Number of Threads (Users) set value 30
               . Ramp-up period (seconds) set value 10
               . Check "Infinite checkbox"
               . Check "Specify Thread lifetime"
               . Duration (seconds) set value 120

     . Now describe about above configuration
          . Number of threads means number of request will generate
          . Ramp-up period 10 ( you can use according to your need) means (In our example 30 threads are used and ramp-up period is 10
               then jmeter will take 10 seconds to get all 30 threads up and running.Each threads will start 0.3 sec (10/30) after the
               previous thread was begun
          . Duration means how long we will run the load test. In our case 120 seconds

          . Now we need to specify the Http request
               . From the left side right click on thread group then "add->sampler->Http Request"
               . We will see another left menu under Thread Group menu.
               . Click on the above menu look at right right. we will fillup some input field to setup which endpoint we want to load test
               . Specify a name for the endpoint in name input field (example: w3school load test)
               . After that add "https or http" in Protocols(http) field and add domain name or ip (example: w3school.com)
                    in "server name or ip" input field and enter port number (example: 443) if required in "Port number" input field
               . Then choose method name (Get/Post) from Http request dropdown and enter URI in path input field ( example: /html/canvas)
               . We can also set parameter / query parameter for the request
               . Select parameter tab below path input field and click add button at the bottom of the window. New row will appear
               . Then add parameter in Name field add parameter name like ('id') and set value in value field like (10)
               . We can add multiple parameter by clicking in add button at the bottom
               . We can also set request body in "Body data" tab for POST request

          . We can also set header for the request
               . From left menu click on Http Request menu then "add -> Config Element -> Http Header Manager"
               . New menu will appear under Http Request menu click on this menu look at the right panel
               . In the last section add header by clicking add button at the bottom
               . If click on add button new row will appear with two field "name" and "value"
               . Add key name like "Accept-Language" and set "en/bn" in the value field
               . We can add multiple header like "Authorization" in name field and "Bearer 12dsfsf323232323sfsfsf" in the value field


          . Now its time to show output. To do so
               . Click on Http Request menu then " add -> Listener -> View Results Tree"
               . Click on Http Request menu then " add -> Listener -> Summary report"
               . Click on Http Request menu then " add -> Listener -> View results in table"
               . Add another option "add -> Timer -> jp@gc - Throughput Shaping Timer"

          . Now discuss about all these above functionality
               . 
   

   . Jenkins setup and configuration (21-26) august 2023