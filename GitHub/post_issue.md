# GitHub apiによるIssue投稿
認証が必要となるため、あらかじめトークンを生成しておく必要がある。トークンはヘッダに置く。  
Issueのフィールドは、これを参考にする。  
[Create an issue](https://developer.github.com/v3/issues/#create-an-issue)
```php
<?php
echo json_decode(get_json(), ture);

function get_json(){
  $base = "https://api.github.com/repos/ivoryworks/til/issues";
  $curl = curl_init();
  curl_setopt_array($curl, [
      CURLOPT_URL => $base,
      CURLOPT_HTTPHEADER => [
          "Content-Type: application/json",
          "Authorization: token " . "d546e5c.......",
          "User-Agent: Mozilla/5.0 (Windows NT 6.1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/47.0.2526.111 YaBrowser/16.3.0.7146 Yowser/2.5 Safari/537.36"
      ],
      CURLOPT_POSTFIELDS => '{
          "title": "Issue api test",
          "body": "Issue Body"
      }'
  ]);

  $content = curl_exec($curl);
  echo $content;
  curl_close($curl);
  return $content;
}
?>
```
