# dingtalk
钉钉服务器API，支持发送工作通知和机器人消息

## 初始化
```php
$dd = new \Everalan\DingTalk\DingTalk([
    'appKey' => 'dingxxxxx',
    'appSecret' => 'Y75DULKtrpu_xxxxx',
]);
```

## 发送工作通知
```php
$message = new \Everalan\DingTalk\Messages\Text('@张三 测试消息');
$dd->sendWorkNotice('024246103336342620', $message, 241709217);
```

## 发送机器人消息
```php
$message = new \Everalan\DingTalk\Messages\ActionCard('公司春游你参加吗？', 'markdown text');
$message->addButton('参加', 'http://www.baidu.com');
$message->addButton('拒绝', 'http://www.weibo.cn');
$message->btnOrientation(1);

$dd->sendBot('c02ff0eb36f41a6ecd753xxxxxxxxxx',$message);
```