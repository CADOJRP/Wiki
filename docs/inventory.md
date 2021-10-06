# Inventory Tutorial
The inventory system on CADOJRP may seem complicated at first but be assured that it is actually pretty simple.

![](https://c.file.glass/cecj6.png)

```input
https://raw.githubusercontent.com/qbcore-framework/txAdminRecipe/main/qbcore.yaml
```
![](https://c.file.glass/6e30e.png)
3) Press save and we recommend txAdmin choose the place to save data.
4) After the recipe finishes installing, press start server if it has not yet started. Once it has started, let it run through the basic resources such as yarn and webpack which need to build up. Once they have builded up, restart the server from the txAdmin interface and there you go, your **first QBCore server**.

## Manual Installation
1) Go into your resources folder for your server.
2) Download the dependecies, core resources which you can find in [here](./other/servercfg?id=qbcore-server-cfg), and other resources you plan to use.
3) Add them in your resources folder.
4) Ensure them in your server cfg by adding the following for every resource.
```cfg
ensure resourceName
```
5) Open ghmattimysql and go to the `config.json` file and configure it based on your database info.
```json
{
    "user": "root",
    "password": "password",
    "host": "localhost",
    "port": 3306,
    "database": "ghmattimysql"
}
```
Now go to your `server.cfg` file and delete the following if it exists.
```cfg
# Database Connection String
set mysql_connection_string "mysql://user:password@host/database?debug=true&charset=utf8mb4"
```
If you would **RATHER** use the method you just deleted, then just delete the `config.json` from ghmattimysql. 😊