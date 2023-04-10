# 【OpenAI】Whisper で音声データを文章化し、発話の開始時間と終了時間を含めたCSVデータにする
- OpenAIが公開している Wisper を利用して、音声データを文章化する
- 文章化するとある程度で区切られて出力され、その区切られた文章の開始時間と終了時間を含めCSVデータにする

## 実行方法

※ 適当な音声データをご準備ください

1. [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/takeshitayy/openai-whisper/blob/main/openai_whisper.ipynb) をクリックして、Google Colaboratory で開く
1. ランタイムの設定
    1. メニューバーの [ランタイム] - [ランタイムのタイプの変更] をクリック
     ![ランタイムのタイプの変更](https://docs.google.com/drawings/d/e/2PACX-1vTo2XkKxxwux9ATDbSPQI0PbJHMYzTJPKwUcUtIj8UwlT_h4sFm9vJtdjusib3p0nNX-j7lYX0EyWu1/pub?w=601&h=545)

    1. ハードウェア アクセラレータ で `GUP` を設定する
    ![ランタイムのタイプの変更](https://docs.google.com/drawings/d/e/2PACX-1vQL7egTWuLu9NOLb5-Z1uZCwIa9dMKraLhn6T6B3KO0_GdYhawWdOyKQaE0SlBDZ0gDr1xAUp0aCPAQ/pub?w=644&h=340)

1. 音声データの準備
    1. サイドバーの 📁アイコン をクリックしてファイルの一覧を表示し、テキストを抽出したい 音声データ を drag & drop で追加
    ![音声データの追加](https://docs.google.com/drawings/d/e/2PACX-1vQU_evi3lR57aAgoRfJhAr5FYpGBf10uA85v8Dx25rE-HMAauXwX1ON0o9KcBVyXvUjqR4H8_rMadCM/pub?w=525&h=307)
    1. 追加した 音声データ を右クリックして `パスをコピー` でファイルの絶対パスをコピーする
    1. 変数 `audioPath` に音声データの絶対パスをセット
1. そのほか設定
    1. 変数 `outputCsvName` に出力するcsvのファイル名をセット
    1. 変数 `model`で 使用する whisper のモデルを選択する
1. `Ctrl + F9` ですべてのセルを実行すると
