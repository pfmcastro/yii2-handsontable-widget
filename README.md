Handsontable Widget for Yii2
============================
A minimalist Excel-like grid widget for Yii2 based on [Handsontable](https://github.com/handsontable/handsontable).

Installation
------------
The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Add the repository to your `composer.json` file.

```
"repositories": [
    {
        "type": "vcs",
        "url": "https://github.com/pfmcastro/yii2-handsontable-widget"
    }
],
```

and add

```json
"himiklab/yii2-handsontable-widget" : "dev-master"
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
To access the javascript representation of the table in a script after creation, use the prefix ```hst``` before the id like:

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
hstTable1.addHook('afterSelectionEnd', function(r, c, r2, c2) {alert(c);});
```

