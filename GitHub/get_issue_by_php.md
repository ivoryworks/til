# PHPでGitHubのissueを取得する
User-Agentを付けないとGitHub apiはエラーを返す。
```php
$curl = curl_init();
curl_setopt_array($curl, [
    CURLOPT_URL => "https://api.github.com/repos/ivoryworks/til/issues/1",
    CURLOPT_HTTPHEADER => [
       "User-Agent: Mozilla/5.0 (Windows NT 6.1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/47.0.2526.111 YaBrowser/16.3.0.7146 Yowser/2.5 Safari/537.36"
    ]
]);
echo curl_exec($curl);
curl_close($curl);
```
