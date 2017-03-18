Persian Date Converting
=======================
Convert Any Type Of Date

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist sgh370/yii2-jdf "dev-master"
```

or add

```
"sgh370/yii2-jdf": "dev-master"
```

to the require section of your `composer.json` file.


Usage
-----

Once the extension is installed, simply use it in your code by  :

```php

1) add the following line in component section in web.config file:
    'components' => [
        ...
        'jdf' => [
            'class' => '\sgh370\jdf\Jdf'
        ],
        ...
    ]

2) use the following functions and pass needed arguments:
    \Yii::$app->jdf->jdate($format, $timestamp = '', $none = '', $time_zone = 'Asia/Tehran', $tr_num = 'fa');
    \Yii::$app->jdf->jstrftime($format, $timestamp = '', $none = '', $time_zone = 'Asia/Tehran', $tr_num = 'fa');
    \Yii::$app->jdf->jmktime($h = '', $m = '', $s = '', $jm = '', $jd = '', $jy = '', $none = '', $timezone = 'Asia/Tehran');
    \Yii::$app->jdf->jgetdate($timestamp = '', $none = '', $timezone = 'Asia/Tehran', $tn = 'en');
    \Yii::$app->jdf->jcheckdate($jm, $jd, $jy);
    \Yii::$app->jdf->tr_num($str, $mod = 'en', $mf = '٫');
    \Yii::$app->jdf->jdate_words($array, $mod = '');
    \Yii::$app->jdf->gregorian_to_jalali($gy, $gm, $gd, $mod = '');
    \Yii::$app->jdf->jalali_to_gregorian($jy, $jm, $jd, $mod = '');

```