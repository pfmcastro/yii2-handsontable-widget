Handsontable Widget for Yii2
============================
A minimalist Excel-like grid widget for Yii2 based on [Handsontable](https://github.com/handsontable/handsontable).

Installation
------------
The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist "himiklab/yii2-handsontable-widget" "*"
```

or add

```json
"himiklab/yii2-handsontable-widget" : "*"
```

to the require section of your application's `composer.json` file.

Usage
-----

```php
use himiklab\handsontable\HandsontableWidget;

<?= HandsontableWidget::widget([
    'settings' => [
        'data' => [
            ['A1', 'B1', 'C1'],
            ['A2', 'B2', 'C2'],
        ],
        'colHeaders' => true,
        'rowHeaders' => true,
    ]
]) ?>
```

Note
-----
To access the javascript representation of the table in a script after creation, use the prefix ```hts``` before the id like:

```php
use himiklab\handsontable\HandsontableWidget;

<?= HandsontableWidget::widget([
    'id' => 'Table1',
    'settings' => [
        'data' => [
            ['A1', 'B1', 'C1'],
            ['A2', 'B2', 'C2'],
        ],
        'colHeaders' => true,
        'rowHeaders' => true,
    ]
]) ?>
```

```javascript
htsTable1.addHook('afterSelectionEnd', function(r, c, r2, c2) {alert(c);});
```

