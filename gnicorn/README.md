
gunicornでflaskを動かすサンプル。    
この後にする設定の例としては、    
gunicornをlinuxのサービスに登録したり、    
nginxと繋いだりする必要がある。    
mac上で確認。    


```
# 動作のテスト
flask run --host '0.0.0.0'

# 実行テスト　その２
python3 main.py


# gunicornで実行
# wsgi は、.py 拡張子を除いたファイル名
# app は、ファイル内の Flask アプリケーションのインスタンス名。

gunicorn --workers 4 --bind 0.0.0.0:5000 wsgi:app

```

確認    

http://localhost:5000/

