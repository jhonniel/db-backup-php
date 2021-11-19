# Database Backup Library 
## Initialize
```php
include('db_backup_library.php');
$dbbackup = new db_backup;
```

Just Use `include()` or `require() ` to the `'db_backup_library.php'` File
And create an object of `'db_backup'` class


## Methods
	
* [connect()](#connect)
* [backup()](#backup)
* [tables()](#tables)
* [download()](#download)
* [save()](#save)
* [db_import()](#db_import)

### `connect()`
**This is an Opotional Method**
If your project connected with Server and database already then you don't need to use this Method,
Other wise you can use this method to connect with MySQL Server and Database
	
**Example**
	
```php 
include('db_backup_library.php');
$dbbackup = new db_backup;
$dbbackup->connect("Server Name", Username, passwrd, Database)
```

### `backup()`
**This is a Mendatory Method**
After connecting with Server and Database you must call this method other wise other method cannot work.

**Example**
```php
include('db_backup_library.php');
$dbbackup = new db_backup;
$dbbackup->connect("ServerName","Username","passwrd","Database");
$dbbackup->backup();
```

	
### `tables()`
If you need to show the name of all tables in database just call this method it will return an array with the name of all tables in the database.
	
**Example**
```php	
include('db_backup_library.php');
$dbbackup = new db_backup;
$dbbackup->connect("ServerName","Username","passwrd","Database");
$dbbackup->backup();
print_r($dbbackup->tables());
```

### `download()`
If you want to download The database you can use this method. After run this method you will see a Download Popup menu of database SQL file.
	
**Example**
```html
<a href="download.php">Download</a>
```
	
**'download.php' Contain Only This code:**
	
```php 
include('db_backup_library.php');
$dbbackup = new db_backup;
$dbbackup->connect("ServerName","Username","passwrd","Database");
$dbbackup->backup();
$dbbackup->download();
```

#### Note: This is the better way to keep the download code into a single page.

### `save()`
If you want to save the backup file into a server directory you can use this method
#### Parameters
It has 2 Parameters
> 1st parameter is Target path (where you want to save the file) *It is Mendatory* If you want to kip it blank you can just use `save("")`
	
> 2nd Parameter is (Optional) name of The file Default is *'backup_yyy-mm-dd.sql'*
	
**Example**
	
```php
include('db_backup_library.php');
$dbbackup = new db_backup;
$dbbackup->connect("ServerName","Username","passwrd","Database");
$dbbackup->backup();
$dbbackup->save("file/","backup"));
```
### db_import()
To Import the SQL File into your Database you can use this method just call the method with the source path of sql file as parameter Then it will import your database
	
#### Parameters
It has 1 Parameters
> The parameter is source path of sql file.
	
**Example**
	
```php
include('db_backup_library.php');
$dbbackup = new db_backup;
$dbbackup->connect("ServerName","Username","passwrd","Database");
$dbbackup->backup();
$dbbackup->db_import("test.sql"));
```
	

<i>Follow me around the web:</i><br>


<a href="https://discord.gg/MM4Phpn4ja"><img src="https://img.shields.io/static/v1?logo=discord&label=&message=Discord&color=36393f&style=flat-square" alt="Discord"></a>
[![Github](https://img.shields.io/badge/-Github-000?style=flat&logo=Github&logoColor=white)](https://github.com/jhonniel)
<a href="https://www.instagram.com/jhanniel_jry/" target="_blank"><img src="https://img.shields.io/badge/Instagram-%23E4405F.svg?&style=flat-square&logo=instagram&logoColor=white" alt="Instagram"></a>
<a href="https://www.facebook.com/contactmejry" target="_blank"><img src="https://img.shields.io/badge/Facebook-%231877F2.svg?&style=flat-square&logo=facebook&logoColor=white" alt="Facebook"></a>
<a href="https://open.spotify.com/user/4xsrtauclcip8cf8fufvfe0d7" target="_blank"><img src="https://img.shields.io/badge/Spotify-%231ED760.svg?&style=flat-square&logo=spotify&logoColor=white" alt="Spotify"></a>
<a href="https://devjry.web.app/" target="_blank"><img src="https://img.shields.io/badge/DEV-%230A0A0A.svg?&style=flat-square&logo=DEV.to&logoColor=white" alt="DEV.to"></a>
