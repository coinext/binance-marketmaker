# binance-marketmaker
Simple Trading Bot (still pre-alpha!). Connects to your binance account and tries to trade between 2 coins only accepting orders that will generate win. Needs https://github.com/binance-exchange/binance-java-api

Installation
============

## Clone and build binance-exchange/binance-java-api:

I have forked the original api to be able to implement minor extensions easily. Also there is a major bug in the original API (regarding multi-tenancy) that is fixed in this version: https://github.com/h-e-n-r-y/binance-java-api branch henry-master.

	cd ~/git
	git clone https://github.com/h-e-n-r-y/binance-java-api
	cd binance-java-api
	mvn install
	
## Build binance-marketmaker:
	cd ~/git
	git clone https://github.com/h-e-n-r-y/binance-marketmaker.git
	cd binance-marketmaker/marketmaker
	mvn install

## Start
	mvn spring-boot:run
	
Access your Marketmaker at http://localhost:8080/

First you must register a user and upload your api-key.

## Install your binance-api-key

Create your API-Key here: https://www.binance.com/userCenter/createApi.html
Edit your profile and fill in api-key and secret.

## Access the H2-Database

Log in as sa (Password can be set in application.properties: db.sa.password). You are automatically redirected to the H2 Database Console. Use the JDBC URL jdbc:h2:~/h2/marketmaker.

## Disclaimer

The app has lots of bugs and it's state is far from being ready! 
These bugs may lead to major loss!
Be careful to understand the sourcecode before using it for dealing with high amounts of coins!

I appreciate comments, bugreports and suggestions for further development...

## Thanks

Thanks, Christopher Downer, for sharing the coin icons. Check out his project here: https://github.com/cjdowner/cryptocurrency-icons

Henry
