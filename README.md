ロケット打ち上げ用の目覚ましです。
私の安眠を守るために、Twitterから情報を取得して、打ち上げが延期になったときは鳴らないようになっています。

使用する際は、別途アラーム音源ファイルを用意して、「alarm_clock.wav」という名前で同フォルダに置いてください。

設定ファイルは「config.ini」で、書式は以下のようになります。

Launch_Time: 打ち上げ時刻です  
Wake_Up_Minutes: 打ち上げの何分前に起こすかの指定  
Target_Twitter_User: 延期情報を取得するTwitterアカウント  
Keyword: この単語から始まるツイートがあれば延期と判断する  

例:

    [LAUNCH]
    Launch_Time = 2020-07-19 05:15:00
    Wake_Up_Minutes = 10
    
    [TWITTER]
    Target_Twitter_User = SpaceflightNow
    Keyword = SCRUB

各社の公式アカウントは書式がバラバラで延期かどうかの判断が難しいため、
基本的に、延期情報はSpaceflightNowから取得します。
SpaceflightNowは、延期のときは冒頭で「SCRUB」とツイートする場合が多いので。

*【注意】*

延期なのに検出に失敗して鳴ったときは無駄に起きるだけなので良いですが、
打ち上げるのに鳴らなかったらダメージが大きいです。
PCのスリープはオフにしておきましょう。
本番前に、一度config.iniを15分後くらいに書き換えて、ちゃんと大音量で鳴るかどうか
テストしておくことをオススメします。
