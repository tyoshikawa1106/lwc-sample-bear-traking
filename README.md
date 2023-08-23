# Salesforce DX Project
Lightning Web コンポーネントを使用した熊追跡アプリケーションの作成  
https://trailhead.salesforce.com/ja/content/learn/projects/lwc-build-flexible-apps?trail_id=build-lightning-web-components

## Table of Contents
- [Requirements](#requirements)
- [Usage](#usage)
- [Link](#link)

## Requirements
- Visual Studio Code 1.81.1 (Universal)
- @salesforce/cli/2.4.10 darwin-arm64 node-v20.5.1

## Usage
### Setup
プロジェクトディレクトリ
```
/Users/<your directory>/projects/salesforce/workspace/
```

GitHubからプロジェクトをダウンロードしてVSCodeで開く。
```
git clone git@github.com:tyoshikawa1106/sf-bear-traking.git
cd sf-bear-traking
code .
```

ハンズオン組織の認証 (CLIログイン)
```
sf org login web -a bear-tracking -b chrome
```

認証組織の一覧表示
```
sf org list
```

ハンズオン組織にソースをデプロイ
```
sf project start deploy -o bear-tracking
```

ハンズオン組織のシステム管理者ユーザに権限セットを割り当て
```
sf org assign permset -n Ursus_Park_User -o bear-tracking
```

ハンズオン組織にテストデータをインポート
```
sf data import tree -p data/plan.json -o bear-tracking
```

ハンズオン組織をChromeブラウザで開く
```
sf org open -o bear-tracking -b chrome
```

アプリケーションランチャーから「Ursus Park」アプリケーションを選択。  
(Application Launcher → Ursus Park)

### Edit Lightnign Page
Home ページにLightning Web コンポーネントを配置
- LWC「bearList」を配置
- LWC「bearMap」を配置
- LWC「helloWebComponent」配置

Bears レコードページにLightning Web コンポーネントを配置
- LWC「bearLocation」を配置
- LWC「bearSupervisor」を配置

## Link
- [trailheadapps/build-apps-with-lwc](https://github.com/trailheadapps/build-apps-with-lwc)
- [Lightning Web Component Trail](https://trailhead.salesforce.com/ja/content/learn/trails/build-lightning-web-components)
