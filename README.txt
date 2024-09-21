//build version: 1.0.1
- Added custom command system.
- Bug fixes.

======================================== SETUP UZER PANEL =========================================

Tested on [
    System  - Ubuntu 20.04
    Ram     - 2 GB
    Cpu     - 1 core
    Ssd     - 30GB
    Network - 1gbps
]

*********** STER 1 (DOWNLOAD) ************
Download zip archive from https://t.me/uzerpanel

******* STEP 2 (CONFIGUARE SERVER) *******
Enter this command to configuare your server for uzer panel:
$ apt update; apt upgrade -y; apt install unzip screen -y; unzip release.zip

****** STEP 3 (CONFIGUARE BUILD) *********
Type: cd release; chmod +x *
Configare uzer config in configs/uzer.json /
	Configuare attack methods in configs/methods.json /
	Configuare plans in configs/plans.json /
Configuare design in assets/*.uzer

************* STEP 4 (RUN) ***************
Start in screen: screen -S uzer and type ./start.sh
Start in not screen: ./start.sh

=========================================== VARIABLES =============================================

<<$USERNAME>> - User nickname.
<<$ID>>" - User telegram id.
<<$NAME>> - Name of stresser in configs/uzer.json["Name"]
<<$PLAN>> - User plan name.
<<$MAXTIME>> - User maximum attack duration.
<<$CONCS>> - User maximum running attacks.
<<$EXPIRED>> - User expired.
<<$PREMIUM>> - User premium (true/false).
<<$ADMIN>> - User admin (true/false).
<<$RUNNING>> - Running attacks of all stresser.
<<$MAX_RUNNING>> - Maximum running of all stresser.
<<TOTAL_ATTACKS>> - Total attacks of all stresser.
<<NETWORK_LOAD>> - Network load in % (0-100).
<<TOTAL_USERS>> - Total users count.
<<PROFIT>> - Total profit.
<<TOTAL_PAID_USERS>> - Total paid users.

=========================================== COMMANDS ==============================================

For add command, create file in assets/commands/command_name.uz (example in assets/commands/test.uz (/test in bot))
For add comment, type # in the beginning
For print data in command line, type log("DATA FOR PRINT")
For send message in bot to user who type command, type send("DATA FOR SEND")
For send request, type request("https://google.com/") and you can use response in log or send with <<$RESPONSE>> variable.
You can use arguments from command (/test args1 args2) with <<$ARGS[1]>> or <<$ARGS[2]>> and etc
You can use return, type return("")

Variables [
    <<$RESPONSE>> if have request("") - request response
    <<$ARGS[N]>> n it args index - arguments
    <<$BUILD_VERSION>> - build version
]



