# 増え続ける公開アプリケーションへの悪意あるアクセス。多層防御を取り入れる SRE 活動

https://sre-next.dev/2023/schedule/#jp026

## Web アプリケーションのセキュリティ対策

- 攻撃者はどんどん新しい手段を取り入れている

### Nist Cybersecurity Framework

### 多層防御

- サービスドメイン
- インフラドメイン
- アプリケーションドメイン

## 城の中の王様を守るために

### エッジ

- Distributed Denial of Service Attack
- L3/L4
- L7
- WAF
  - WAF のログは必ず入れる
- CDN
- 負荷分散、オートスケール
- HTTPS の強制
- セキュリティヘッダーの追加
- オリジンの秘匿
- 悪意のある攻撃に対して 403 を返すことが大切
  - ちゃんと対策しているよと攻撃者に知らせることが大切(403 返すようにしたらピタッと攻撃止まった)
- アプリケーションをホストから分離
  - VM
    - 不要なミドルウェアのアンインストール
  - コンテナ
    - 非特権モードで稼働
    - ReadOnly
    - サンドボックス化
- DB
  - 機密情報は DB に保管
    - ログに出力しない
  - アクセス権の限定
  - バックアップ、リストア
  - クレデンシャルは強度の高いパラメーターストアへ
- 最新バージョンの利用
  - コンテナ、サーバーレスの優位性が発揮される
- 設計段階からセキュリティについて考える必要がある
- 人的ミス
- CSPM
  - クラウドサービスの各種設定がセキュアであることの重要
- モニタリング
  - 攻撃されていることを気づかないかもしれないため、モニタリングを絶対行う
  - 気づかないことは SRE の恥だと思った方が良い
- ロギング
- 正常な状態にすぐ戻せる状態にしておく
  - 乗っ取られた場合でも乗っ取られる前にすぐ戻せる状態にしておく
