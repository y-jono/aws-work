```command
$ aws sns create-topic --name topicsamplebycli
{
    "TopicArn": "arn:aws:sns:ap-northeast-1:918636316746:topicsamplebycli"
}
```

```powershell
#作成
$topic2Json = aws sns create-topic --name topicsamplebycli2

#確認のための出力
$topic2Json > topic2.json

#作成結果をオブジェクト化
$topic2 = ($topic2Json | ConvertFrom-Json)

#削除
aws sns delete-topic --topic-arn $topicArn.TopicArn

#確認
aws sns list-topics
```
