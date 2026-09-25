# Go Nakano

立命館大学 情報理工学部 実世界情報コースのB4です。  
Webアプリケーション開発を中心に学びながら、身近な業務の困りごとを解決するツールの開発・運用や、Unity / C# によるVRシステムのチーム開発に取り組んでいます。

## About Me

- Webアプリケーション開発に関心があり、ブラウザからサーバー・データベースまでのつながりを学んでいます
- 塾の業務で使うDiscord Botを開発し、2026年7月から実際に運用しています
- FlaskとSQLiteを用いて、認証付きの成績管理Webアプリを個人開発しました
- 研究室のチーム開発で、体感型VRグライダーシミュレータのメインゲームシーンを担当しました
- Git / GitHub / SourceTreeを用いたチーム開発経験があります

## Interests

- Web Application Development
- Business Automation / Bot
- VR / XR
- Sensor-based Interaction
- Human-Computer Interaction
- Team Development

## Tech Stack

- **Web**：Python / Flask、SQLite、HTML / CSS / JavaScript、Chart.js
- **Bot・自動化・運用**：discord.py、Playwright、Oracle Cloud、Linux / systemd、pytest
- **VR・デバイス連携**：Unity / C#、Meta Quest 3、ESP32、WebSocket / TCP
- **開発**：Git / GitHub、SourceTree

## Projects

### Discord Bot for Attendance Management

塾の入退室ログを、普段使っているDiscordのスラッシュコマンドから確認できるPython製Botです。  
生徒ごとの直近1週間の入退室時刻と滞在時間を表示します。2026年7月29日から塾のDiscordサーバーで稼働しています。

- 入退室管理システムのCSV出力操作をPlaywrightで自動化し、10分ごとに最新データを取得
- 取得したCSVの形式を検証してから差し替え、取得に失敗しても前回の正常なデータで応答
- Oracle Cloud Always Free上でsystemdにより常時稼働し、更新が止まると管理者にDMで通知

最初の版は外部APIを利用していましたが、入退室管理システムの変更でAPIが使えなくなったため、CSV取得方式に作り直しました。  
現在運用している後継版のソースコードは非公開で、公開しているのは旧API版です。

- [nyutai-discord-bot](https://github.com/GoNakano/nyutai-discord-bot)（旧API版）

### Student Grade Management App

成績HTMLを手動で貼り付け、単位・GPA/GPSを整理・可視化するFlask製の非公式個人開発アプリです。  
ユーザー登録・ログイン、ユーザーごとのデータ分離、成績表HTMLの解析、GPAと取得単位のグラフ表示を実装しています。  
成績情報や個人情報を扱うため、ローカル環境での利用を想定しています。

- [seiseki-kanri-public](https://github.com/GoNakano/seiseki-kanri-public)
- デモ：[seiseki-kanri.onrender.com](https://seiseki-kanri.onrender.com)（サンプルデータで確認できます。初回表示に時間がかかる場合があります）

### VR Glider Simulator

研究室のチーム開発プロジェクトとして、身体の傾きを利用した体感型VRグライダーシミュレータを開発しました。  
IMUセンサーによる姿勢入力、UnityによるVR空間、Meta Quest 3、ESP32との通信を組み合わせたシステムです。

主に以下を担当しました。

- メインゲームシーン
- ゲーム進行管理
- UI / HUD
- ボーナスリング・チェックポイント・ゴール処理
- リザルト表示
- サウンド制御の枠組み
- TCP通信による外部機器連携
- パフォーマンス改善
- Git / GitHubを用いたチーム開発統合

※研究室のPrivateプロジェクトのため、ソースコードは公開していません。  
公開可能な範囲の概要は以下にまとめています。

- [vr-glider-project-summary](https://github.com/GoNakano/vr-glider-project-summary)
