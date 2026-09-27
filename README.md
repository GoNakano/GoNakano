# 中野 剛 (Go Nakano)

立命館大学 情報理工学部 実世界情報コースのB4です。  
実装にはAI（Claude Code・Codex）を使い、自分は課題の整理・要件決め・動作確認・運用を担当しています。Web開発は現在学習中です。

## About Me

- 塾の入退室記録をDiscordから確認できるBotを作り、2026年7月から塾で使われています
- 研究室のチーム開発で、体感型VRグライダーシミュレータの制作に参加しました
- 海外インターン（インド・Sasken Technologies）で、車載向けの前方衝突警告を評価ボードで動かすチーム開発に参加しました
- HTML / CSS / JavaScript とWebの仕組みを書籍で学習中です
- AtCoderでPythonを使って問題を解いています

## 使ったことのある技術

- **Python**：AtCoder
- **Bot・運用**：Discord Bot、Playwright、Oracle Cloud、Linux / systemd（AIを使って構築し、運用しています）
- **VR・デバイス**：Unity、Meta Quest 3、ESP32（研究室のチーム開発）
- **組み込み**：TI TDA4VM評価ボード、TI Processor SDK、Ubuntu（海外インターン）
- **開発**：Git / GitHub、SourceTree
- **学習中**：HTML / CSS / JavaScript

## Projects

### Discord Bot for Attendance Management

塾の入退室ログを、普段使っているDiscordのスラッシュコマンドから確認できるBotです。  
生徒ごとの直近1週間の入退室時刻と滞在時間を表示します。2026年7月29日から塾のDiscordサーバーで稼働しています。

自分が担当したこと

- 入退室の確認に手間がかかっている課題を見つけ、必要な機能（生徒名で検索して直近1週間の記録を見る）を決めた
- サーバーの用意、再ログインなどの日々の運用、不具合の原因の切り分けと動作確認

実装はAIを使って行いました。管理画面のCSV出力をPlaywrightで自動取得し、Oracle Cloud Always Free上で常時稼働しています。

- [takeda-log-discord-bot](https://github.com/GoNakano/takeda-log-discord-bot)（現在運用している版）
- [nyutai-discord-bot](https://github.com/GoNakano/nyutai-discord-bot)（外部APIを使っていた旧版）

### VR Glider Simulator

研究室のチーム開発で、身体の傾きで操作する体感型VRグライダーシミュレータを制作しました。  
IMUセンサーによる姿勢入力、Unity、Meta Quest 3、ESP32との通信を組み合わせたシステムです。

自分が担当したこと

- メインゲームシーンの進行（カウントダウン、リング・チェックポイント・ゴールの判定、リザルト、サウンドなど）の作成と調整。C#のコードはAIで生成し、Unity上で組み込んで調整しました
- 子供向けモードなど、体験者に合わせた難易度や進行の調整
- Gitでのブランチ統合と、チームへのSourceTreeの使い方の共有
- Quest 3・センサー・ESP32をつないだ実機での試験と不具合対応

※研究室のPrivateプロジェクトのため、ソースコードは公開していません。

- [vr-glider-project-summary](https://github.com/GoNakano/vr-glider-project-summary)

### Forward Collision Warning on an Embedded Board（海外インターン）

立命館大学の海外インターンシップで、インド・ベンガルールのSasken Technologiesに約4週間参加しました（2026年8〜9月）。  
学生5名のチームで、走行映像から前方の車両を検出して衝突までの時間を推定し、警告を出すシステムを、Pythonで試作してからCに移し、TI TDA4VMの評価ボード上で動かしました。

自分が担当したこと

- ボード用SDKのセットアップ、Ubuntuでのビルド、評価ボードでの実行と動作確認
- メンバーのブランチの統合（Git）
- 動画入力と警告処理（C）の、ボードの物体検出アプリへの統合。コードの編集には生成AIを使い、ビルドと実機での確認は自分で行いました
- 英語での成果発表（評価ボードのセットアップ、個人の貢献、まとめを担当）

- [sasken-fcw-internship-summary](https://github.com/GoNakano/sasken-fcw-internship-summary)

### Student Grade Management App

FlaskとSQLiteで作った、非公式の成績管理Webアプリです。AIを使って作成しました。

- [seiseki-kanri](https://github.com/GoNakano/seiseki-kanri)
- デモ：[seiseki-kanri.onrender.com](https://seiseki-kanri.onrender.com)（無料枠のため、初回表示に1分ほどかかる場合があります）
