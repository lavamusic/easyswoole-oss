# oss

## 阿里云调用
```php
<?php
/**
 * Created by PhpStorm.
 * User: Tioncico
 * Date: 2019/11/20 0020
 * Time: 15:28
 */
include "./vendor/autoload.php";
include "./phpunit.php";

go(function (){

    $config = new \EasySwoole\Oss\AliYun\Config([
        'accessKeyId'     => ACCESS_KEY_ID,
        'accessKeySecret' => ACCESS_KEY_SECRET,
        'endpoint'        => END_POINT,
    ]);
    $client = new \EasySwoole\Oss\AliYun\OssClient($config);
    $data = $client->putObject('tioncicoxyz','test',__FILE__);
    var_dump($data);
});
```