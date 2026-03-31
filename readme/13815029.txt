#PECL extension for reading StarDict
Cloned from https://code.google.com/p/php-stardict/

StarDict is a powerful open-source dictionary app, this extension brings the very power to the world of PHP

###Installation

```
phpize
./configure --enable-sdict
make
sudo make install
```

###Testing code

```php
  $dic = sdict_popen('/usr/share/dict');
  var_dump(sdict_query($dic, 'lama'));
  sdict_close($dic);
```
