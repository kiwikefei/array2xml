- support php 5.6+
- support Silverstripe 3.6
```php
    public function run($request)
    {
        $array = [
            'Hello' => [
                '_attributes' => [
                    'attr1' => 'value1',
                    'attr2' => 'value2',
                    'attr3' => 'value3',
                    'attr4' => 'value4'
                ],
                'name' => 'This one',
                'AAA' => [
                    '_cdata' => '<h1>HTML data</h1>',
                ],
                'hi' => ''
            ],
            'World' => [
                'name' => '<h1>parsed HTML data</h1>',
				'other' => 'Other thingy'
            ]
        ];
        $root = [
            'rootElementName' => 'OneRoof',
            '_attributes' => [
                'xmlns' => 'http://some.com/xmlns',
            ],
        ];
        $result = ArrayToXml::convert($array, $root);
        d($result);
    }
```
