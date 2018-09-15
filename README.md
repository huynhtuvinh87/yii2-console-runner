# yii2-console-runner
This is component for running console command in yii2 web applications

## Installation

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

To install, either run

```
$ composer require huynhtuvinh87/yii2-console-runner "*"
```

or add

```
"toriphes/yii2-console-runner": "*"
```

to the ```require``` section of your `composer.json` file.

## Usage

You can user yii2-console-runner importing the class file
```php
use huynhtuvinh87\console\Runner;
$output = '';
$runner = new Runner();
$runner->run('controller/action param1 param2 ...', $output);
echo $output; //prints the command output
```

or using it like an application component:
```php
//you config file
'components' => [
    'consoleRunner' => [
        'class' => 'toriphes\console\Runner'
    ]
]
```
```php
//some application file
$output = '';
Yii::$app->consoleRunner->run('controller/action param1 param2 ...', $output);
echo $output; //prints the command output
```

