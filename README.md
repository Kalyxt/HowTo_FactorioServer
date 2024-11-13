# HowTo_FactorioServer
Docs on how to start Factorio headless server

# Windows

- In order to start server, you need to have file with game settings, this can be obtained by copying `server-settings.example.json` located in `C:\Program Files (x86)\Steam\steamapps\common\Factorio\data`. 
- Make a copy of it and rename it to `servername-server-settings.json`. 
- You can change various server properties here, like name, description, save interval etc, but most important is your factorio user name and token, that can be generated after you log in at www.factorio.com.
- You can specify server admin list in `servername-server-admin-list.json` like. Add more players separated by comma. 
`[
  "Kalixt"
]`
- Create empty `.bat` file in `C:\Program Files (x86)\Steam\steamapps\common\Factorio\bin\x64` with following parameters. `start /wait .\factorio.exe --start-server-load-latest --server-settings "C:\Program Files (x86)\Steam\steamapps\common\Factorio\data\servername-server-settings.json" --server-adminlist "C:\Program Files (x86)\Steam\steamapps\common\Factorio\data\servername-server-admin-list.json"`.
- If it stops for any reason and you want to see error message, add PAUSE to the .bat file, this prevent command line window from automatically closing.

