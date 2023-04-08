# 【OpenAI】Whisper で音声データを文章化し、発話の開始時間と終了時間を含めたCSVデータにする
- OpenAIが公開している Wisper を利用して、音声データを文章化する
- 文章化するとある程度で区切られて出力され、その区切られた文章の開始時間と終了時間を含めCSVデータにする

## 実行方法

※ 適当な音声データをご準備ください

1. [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/takeshitayy/openai-whisper/blob/main/openai_whisper.ipynb) をクリックして、Google Colaboratory で開く
1. ランタイムの設定
    1. メニューバーの [ランタイム] - [ランタイムのタイプの変更] をクリック
    1. ハードウェア アクセラレータ で GUP を設定する
1. 音声データの準備
    1. 📁アイコンをクリックしてファイルの一覧を表示
    1. テキストを抽出したい 音声データ を drag & drop で追加
    1. 追加した 音声データ を右クリックして パスをコピー でファイルの絶対パスをコピーする
    1. audioPath: 音声データ の絶対パスをセット
1. そのほか設定
    1. outputCsvName: 出力するcsvのファイル名をセット
    1. model: whisper のモデルを選択する
1. Ctrl + F9 ですべてのセルを実行する
