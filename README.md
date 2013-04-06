#csv2plist

Simple script to convert CSV file to plist file.


##Usage


````
$ php csv2plist.php hoge.csv
````

When the CSV file has title row, use -t option.

````
$ php csv2plist.php -t hoge.csv
````

##Example

(sample.csv)

````
id,name,age,birth
0,tsutsumi,32,5/26
1,sato,27,1/11
2,tanaka,21,11/3
````        

(command)

````
$ php csv2plist.php -t sample.csv
````

(generated plist)

````
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<array>
	<dict>
		<key>id</key>
		<string>0</string>
		<key>name</key>
		<string>tsutsumi</string>
		<key>age</key>
		<string>32</string>
		<key>birth</key>
		<string>5/26</string>
	</dict>
	<dict>
		<key>id</key>
		<string>1</string>
		<key>name</key>
		<string>sato</string>
		<key>age</key>
		<string>27</string>
		<key>birth</key>
		<string>1/11</string>
	</dict>
	<dict>
		<key>id</key>
		<string>2</string>
		<key>name</key>
		<string>tanaka</string>
		<key>age</key>
		<string>21</string>
		<key>birth</key>
		<string>11/3</string>
	</dict>
</array>
</plist>
````


##License

MIT