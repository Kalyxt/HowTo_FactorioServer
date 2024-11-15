# HowTo_FactorioServer
Docs on how to start Factorio headless server
This not cover how to set up networking and port forward.

# Windows

- You need copy of factorio, the best would be have it from steam, so you can easily update to latest game version. <br>
- In order to start server, you need to have file with game settings, this can be obtained by copying `server-settings.example.json` located in `C:\Program Files (x86)\Steam\steamapps\common\Factorio\data`. <br>
- Make a copy of it and rename it to `servername-server-settings.json`.  <br>
- You can change various server properties here, like name, description, save interval etc, but most important is your factorio user name and token, that can be generated after you log in at www.factorio.com. <br>
- You can specify server admin list in `servername-server-admin-list.json` like. Add more players separated by comma. <br>
`[
  "Kalixt"
]`
- Create empty `.bat` file in `C:\Program Files (x86)\Steam\steamapps\common\Factorio\bin\x64` with following parameters. <br> `start /wait .\factorio.exe --start-server-load-latest --server-settings "C:\Program Files (x86)\Steam\steamapps\common\Factorio\data\servername-server-settings.json" --server-adminlist "C:\Program Files (x86)\Steam\steamapps\common\Factorio\data\servername-server-admin-list.json"`. <br>
- If it stops for any reason and you want to see error message, add PAUSE to the .bat file, this prevent command line window from automatically closing. <br>
- Game saves are located in `C:\Users\Username\AppData\Roaming\Factorio\saves`. <br>
