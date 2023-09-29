# Warning アラートを放置しない！アラート駆動でログやメトリックを自動収集する仕組みによる恩恵

https://sre-next.dev/2023/schedule/#jp060
https://speakerdeck.com/mashiike/warningaratowofang-zhi-sinai-aratoqu-dong-deroguyametoritukuwozi-dong-shou-ji-surushi-zu-miniyoruen-hui?slide=13

### Warning アラートの実例

- 平均レスポンスが 500ms
- リクエスト 5XX エラー 1 件

### warning アラートは結構な頻度ででる

### warning アラートの確認

- 週次定例で warning アラートについて振り返るようにする

### warning アラートにまとわるトイル

- 調べるのが手作業
- 週次定例で繰り返し実施される
- サービスの成長に比例してアラートが増える
- 確認作業はマニュアルかしやすく、自動化可能

### 作成したのがアラート駆動でログやメトリクスを自動取集する仕組み

- Webhook 経由で Lambda 関数起動

### prepalert の仕組みはカヤックのテックブログに書いておいた

### 取り入れて良かったこと

- 定例の時間が削減された
- 収集内容の拡充
  - 人が収集すると収集不足とかあるし、意見しにくい
  - 様々なとこから自動でデータを撮ってこれるようになった
- 早期問題の発見
  - あとで調べますとかがなくなって早期問題発見が繋がった。
