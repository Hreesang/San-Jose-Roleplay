# San-Jose-Roleplay
This gamemode is originally from Chrillzen and optimized by Hreesang.
(Original Thread: https://forum.sa-mp.com/showthread.php?t=573694)

[![sampctl](https://shields.southcla.ws/badge/sampctl-San--Jose--Roleplay-2f2f2f.svg?style=for-the-badge)](https://github.com/Hreesang/San-Jose-Roleplay)


![Scratch RP](http://i.imgur.com/BT1OJHt.png)

**Lines:** 25517

**Features:**

- *Dynamic Housing System*
- *Dynamic Faction System*
- *Vehicle Dealership (credits to MadeMan)*
- *Dynamic Business System*
- *All of the necessary Role Play commands.*
- *Busdriver Job, Pizza Stack Job, Fishing Job, 24/7 Job.*
- *Advanced Windows System*
- *Very clean and barely any grammar mistakes.*
- *Death System with textdraws (showing where u got shot and how many times)*
- *Much more!*

```
CMD:commands(playerid, params[])
{
    SCM(playerid, COLOR_WHITE, "_______________________________[SERVER COMMANDS]_______________________________");
    SCM(playerid, COLOR_WHITE, "[GENERAL:] /pay /pm /stats /dice /call /givedrug /animlist /factionhelp /dropgun /refuel /kph /mph /stats /admins /supporters");
    SCM(playerid, COLOR_WHITE, "[GENERAL:] /report /givegun /balance /withdraw /deposit /pickup /hangup /takedrivingtest /notehelp /jobhelp /pickupgun /inv");
    SCM(playerid, COLOR_WHITE, "[GENERAL:] /sms /licenses /greet /v /businesshelp /househelp /fishinghelp /factioninfo /invite /id /coin /ageup /vgivekeys /walk");
    SCM(playerid, COLOR_WHITE, "[GENERAL:] /(ad)vertisement /frisk /train /buy /help /low /do /me /shout /(o)oc /(f)action /windows /removecp /signwelfare /walkstyle");
    SCM(playerid, COLOR_WHITE, "[GENERAL:] /phonehelp /boombox /smoke /drink /usedrug /blockpm /fishingrod /helpme /buydrink /refuel /vsell /map /quitwelfare /list_tickets");
    if(PlayerInfo[playerid][pFaction] == 2)
    {
        SCM(playerid, COLOR_WHITE, "[POLICE:] /arrest /cuff /uncuff /opendoor /closedoor /locker /closecell /opencell /opengate /closegate");
        SCM(playerid, COLOR_WHITE, "[POLICE:] /revokeguns /revokedrugs /(m)egaphone /tazer /(r)adio /revokelicense /vmdc");
        SCM(playerid, COLOR_WHITE, "[POLICE:] /spike /removespike /removeroadblock /roadblock /ticket /takegunrights /mdc /suspect");
    }
    return 1;
}
```

```
CMD:admincommands(playerid, params[])
{
    if(PlayerInfo[playerid][pAdmin] < 1)
    {
        SCM(playerid, COLOR_GREY, "You're not authorized to use this command.");
    }
    if(PlayerInfo[playerid][pAdmin] == 1)
    {
        SCM(playerid, COLOR_WHITE, "_______________________________[SUPPORTER COMMANDS]_______________________________");
        SCM(playerid, COLOR_WHITE, "[SUPPORTERS:] /accepthelpme /ignorehelpme /warn /mute /unmute /freeze /unfreeze");
        SCM(playerid, COLOR_WHITE, "[SUPPORTERS:] /tduty /(a)dminchat /ajail /astats /kick /spectate /spectateoff");
    }
    if(PlayerInfo[playerid][pAdmin] == 2)
    {
        SCM(playerid, COLOR_WHITE, "_______________________________[ADMINISTRATOR COMMANDS]_______________________________");
        SCM(playerid, COLOR_WHITE, "[SUPPORTERS:] /accepthelpme /ignorehelpme /warn /mute /unmute /freeze /unfreeze");
        SCM(playerid, COLOR_WHITE, "[SUPPORTERS:] /goto /gethere /tduty /(a)dminchat /ajail /astats /kick /spectate /spectateoff");
        SCM(playerid, COLOR_WHITE, "[JUNIOR ADMINISTRATORS:] /free /gotofuelstation /editv /setfuel /takegunrights /givegunrights /setskin /setvw /sethp");
        SCM(playerid, COLOR_WHITE, "[JUNIOR ADMINISTRATORS:] /setarmour /rtc /arevokedrugs /arevokeguns /afactionname /asetleader /sendtols /gotols /äslap");
        SCM(playerid, COLOR_WHITE, "[JUNIOR ADMINISTRATORS:] /afactioninfo /afactionrankname /alock /seenames /spectate /spectateoff /ban /unban /unbanip /offlineban");
    }
    if(PlayerInfo[playerid][pAdmin] == 3)
    {
        SCM(playerid, COLOR_WHITE, "_______________________________[ADMINISTRATOR COMMANDS]_______________________________");
        SCM(playerid, COLOR_WHITE, "[SUPPORTERS:] /accepthelpme /ignorehelpme /warn /mute /unmute /freeze /unfreeze");
        SCM(playerid, COLOR_WHITE, "[SUPPORTERS:] /goto /gethere /tduty /(a)dminchat /ajail /astats /kick /spectate /spectateoff");
        SCM(playerid, COLOR_WHITE, "[JUNIOR ADMINISTRATORS:] /free /gotofuelstation /editv /setfuel /takegunrights /givegunrights /setskin /setvw /sethp");
        SCM(playerid, COLOR_WHITE, "[JUNIOR ADMINISTRATORS:] /setarmour /rtc /arevokedrugs /arevokeguns /afactionname /asetleader /sendtols /gotols /aslap");
        SCM(playerid, COLOR_WHITE, "[JUNIOR ADMINISTRATORS:] /afactioninfo /afactionrankname /alock /seenames /spectate /spectateoff /ban /unban /unbanip /offlineban");
        SCM(playerid, COLOR_WHITE, "[GENERAL ADMINISTRATORS:] /agivegun /givemoney /setmoney /agivedrug /alockbiz /asellbiz" );
        SCM(playerid, COLOR_WHITE, "[GENERAL ADMINISTRATORS:] /asellhouse /alockhouse /createhouse /deletehouse /alock /seenames" );
    }
    if(PlayerInfo[playerid][pAdmin] == 4)
    {
        SCM(playerid, COLOR_WHITE, "_______________________________[ADMINISTRATOR COMMANDS]_______________________________");
        
        SCM(playerid, COLOR_WHITE, "[SUPPORTERS:] /accepthelpme /ignorehelpme /warn /mute /unmute /freeze /unfreeze");
        SCM(playerid, COLOR_WHITE, "[SUPPORTERS:] /goto /gethere /tduty /(a)dminchat /ajail /astats /kick /spectate /spectateoff");
        SCM(playerid, COLOR_WHITE, "[JUNIOR ADMINISTRATORS:] /free /gotofuelstation /editv /setfuel /takegunrights /givegunrights /setskin /setvw /sethp");
        SCM(playerid, COLOR_WHITE, "[JUNIOR ADMINISTRATORS:] /setarmour /rtc /arevokedrugs /arevokeguns /afactionname /asetleader /sendtols /gotols /aslap");
        SCM(playerid, COLOR_WHITE, "[JUNIOR ADMINISTRATORS:] /afactioninfo /afactionrankname /alock /seenames /spectate /spectateoff /ban /unban /unbanip /offlineban");
        SCM(playerid, COLOR_WHITE, "[GENERAL ADMINISTRATORS:] /agivegun /givemoney /setmoney /agivedrug /alockbiz /asellbiz" );
        SCM(playerid, COLOR_WHITE, "[GENERAL ADMINISTRATORS:] /asellhouse /alockhouse /createhouse /deletehouse /alock /seenames" );
        SCM(playerid, COLOR_WHITE, "[LEAD ADMINISTRATORS:] /restart");
    }
    return 1;
}
```

**Notes:**

There are some houses and businesses already, but you'll have to create the remaining ones with /createbiz and /createhouse! Check line 11668 for the different types that exist. (If you have edited the gamemode, it's at the createbiz command.

## Setup

### 1. Dependencies

Ensure you have ALL the dependencies listed in the master script (the one you compile from!) each #include line has a link to the release page.

### 2. Compile!

If you set up all the dependencies correctly, there should be *no* errors or warnings at all unless mentioned in the commit message.

### 3. Set up plugins in your `server.cfg` file.

```
plugins sscanf streamer
```
