# libEco
**libEco is a PocketMine-MP virion that makes easy to use API of economy plugins!**

## Installation
You can get the compiled .phar file on poggit by clicking [here](https://poggit.pmmp.io/ci/David-pm-pl/libEco/~).

## Supports
Currently this library only supports BedrockEconomy and EconomyAPI.

## Usage
LibEconomy makes using the economy plugins API easier!.

## Check have any economy installed

```php
use davidglitch04\libEco\libEco;
if(libEco::isInstall()){
// Installed
} else{
// No any eco
}
```
## Get the money of a player

```php
use davidglitch04\libEco\libEco;
libEco::myMoney($player, static function(float $money) : void {
	var_dump($money);
});
```
## Add the money of a player

```php
use davidglitch04\libEco\libEco;
libEco::addMoney($player, $amount);
```

## Reduce the money of a player

```php
use davidglitch04\libEco\libEco;
# OPTION 1
libEco::reduceMoney($player, $amount);
# OPTION 2
libEco::reduceMoney($player, $amount, static function(bool $success) : void {
	if($success){
		//TODO IF SUCCESS
	} else{
		//TODO IF FAIL
	}
});
```