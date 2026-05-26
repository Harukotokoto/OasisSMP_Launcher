macOSネイティブアプリのUI/UXを可能な限り忠実に再現してください。
単なる「Apple風」ではなく、実際のmacOS標準アプリに近い設計・余白・挙動・視覚ルールを目指してください。

## 目的

* macOS Sonoma / Sequoia 系統のネイティブアプリに見えるUI
* Electron製やWeb感を消す
* Finder / Safari / Settings / Music / Xcode などのApple純正アプリに近い体験
* “Apple Human Interface Guidelines” に準拠したデザイン

---

## 参考にするもの

最優先:

* Apple Human Interface Guidelines
* macOS標準アプリ（Finder / Safari / System Settings / Music / App Store / Xcode）

参考URL:

* [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/?utm_source=chatgpt.com)
* [SF Symbols](https://developer.apple.com/sf-symbols/?utm_source=chatgpt.com)
* [Apple Design Resources](https://developer.apple.com/design/resources/?utm_source=chatgpt.com)

デザイン参考:

* macOS Finder
* macOS System Settings
* Xcode Navigator Layout
* Safari Sidebar Design

---

## 必須デザインルール

### 1. ウィンドウ構造

* macOS標準のタイトルバー構造を再現
* 左上に信号機ボタン（close / minimize / fullscreen）
* unified toolbar スタイル
* タイトルバーとツールバーが自然に融合していること
* ウィンドウ角丸はmacOS相当

---

### 2. サイドバー

* Finder風の半透明サイドバー
* 適切な vibrancy / blur
* 選択時はmacOS標準のハイライト
* アイコンはSF Symbolsベース
* セクション間余白を広めに

---

### 3. 配色

* Apple純正アプリのニュートラルトーン
* 過剰な彩度を禁止
* グレー階調を中心に構成
* アクセントカラーのみ強調
* ライト/ダーク両対応

避けるもの:

* Tailwind感の強い原色
* Webアプリ的な濃い影
* Material Design風UI
* Windowsライクな境界線

---

### 4. 余白・レイアウト

* Apple特有の広めの余白
* 情報密度を上げすぎない
* 8pxグリッドではなくmacOSネイティブ寄りの空気感を優先
* セクション間に呼吸感を持たせる

---

### 5. コンポーネント

以下をmacOSネイティブに寄せる:

* sidebar
* segmented control
* toolbar
* search field
* dropdown menu
* context menu
* modal
* table/list
* toggle switch
* tab
* scroll area

---

### 6. タイポグラフィ

* San Francisco (SF Pro) ベース
* フォントウェイトはApple標準に近づける
* 過剰な太字を禁止
* 行間を広めに
* “読みやすさ”を最優先

---

### 7. アニメーション

* macOSらしい自然な easing
* 過度なアニメーション禁止
* hoverは控えめ
* opacity / blur / scale を中心に
* iOSっぽくしすぎない

---

## 実装ルール

* 「Webサイト」ではなく「macOSデスクトップアプリ」として設計
* Electron感を消す
* ブラウザ感を消す
* CSSはApple純正UIの再現を優先
* コンポーネントライブラリ依存を減らす
* Tailwind使用時もTailwind感を完全に消す

---

## 重要

以下のような状態を目標にしてください:

「スクリーンショットだけ見たらApple純正アプリと区別しづらい」

特に:

* Finder
* System Settings
* Safari
* Xcode

の空気感・余白・透明感・階層感を徹底研究してください。

“Appleっぽい”ではなく、“Appleが実際に作ったように見えること”を基準にしてください。