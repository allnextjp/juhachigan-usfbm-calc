# USDS × 十八願物流 送料シミュレーター

## 🚀 概要

FedExとECMSの送料を比較計算するWebアプリケーションです。梱包サイズと重量を入力することで、リアルタイムで送料見積もりを表示します。

## ✨ 主な機能

### 📦 **送料計算機能**
- **正確な料金計算**: 最新の料金表に基づく計算
- **容積重量計算**: FedX ÷5,000 / ECMS ÷6,000
- **0.5kg刻み切り上げ**: 実際の配送業界基準に準拠
- **燃油サーチャージ・割増率**: リアルタイム料金反映

### 📏 **サイズ超過判定**
- 3辺合計 >243cm
- 最長辺 >121cm  
- 2番目の長辺 >76cm
- 超過時の詳細理由表示

### 💰 **料金比較**
- 両サービスの料金を同時表示
- お得な方を自動ハイライト
- 差額とお得度を表示
- 基本料金も併記

### 🎨 **デザイン**
- **十八願物流ブランド**: モノクロ・ミニマリスト
- **レスポンシブ対応**: PC・タブレット・スマートフォン
- **アクセシビリティ**: ARIA対応・キーボードナビゲーション

## 🛠️ 技術仕様

### **フロントエンド**
- **HTML5**: セマンティックマークアップ
- **CSS3**: Flexbox・Grid・アニメーション
- **Vanilla JavaScript**: 外部依存なし

### **計算ロジック**
- **重量計算**: `Math.max(実重量, 容積重量)`
- **切り上げ処理**: `Math.ceil(weight * 2) / 2`
- **最終料金**: `基本料金 × (1 + 燃油サーチャージ + 割増率)`

### **料金設定**
- **FedX**: 燃油サーチャージ 45% + 割増率 25% = 1.7倍
- **ECMS**: 燃油サーチャージ 48.4% + 割増率 50% = 1.984倍

## 📊 料金表（抜粋）

| 重量 | FedX基本料金 | ECMS基本料金 | FedX最終料金 | ECMS最終料金 |
|------|-------------|-------------|-------------|-------------|
| 5.0kg | ¥5,508 | ¥4,329 | ¥9,364 | ¥8,588 |
| 9.0kg | ¥7,630 | ¥6,680 | ¥12,971 | ¥13,253 |
| 15.0kg | ¥12,540 | ¥9,709 | ¥21,318 | ¥19,262 |

## 🚀 デプロイ方法

### **GitHub Pages**
1. リポジトリ設定 → Pages
2. Source: Deploy from a branch
3. Branch: main → / (root)
4. 自動デプロイ開始

### **Netlify**
1. [Netlify](https://app.netlify.com/drop) でドラッグ&ドロップ
2. または GitHub リポジトリ連携
3. 即座に公開URL生成

### **Vercel**
1. GitHub リポジトリをインポート
2. 自動ビルド・デプロイ
3. カスタムドメイン設定可能

## 📁 ファイル構成

```
📦 送料シミュレーター/
├── 📄 index.html          # メインアプリケーション
├── 📄 README.md           # プロジェクト説明書
└── 📄 LICENSE             # ライセンス情報
```

## 🔧 カスタマイズ

### **料金表更新**
`BASE_SHIPPING_RATES` オブジェクトの値を変更

### **燃油サーチャージ・割増率変更**
`SURCHARGES` オブジェクトの値を変更

### **サイズ制限変更**
`SIZE_LIMITS` オブジェクトの値を変更

## 🌐 ブラウザ対応

- ✅ Chrome 90+
- ✅ Firefox 88+  
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ iOS Safari 14+
- ✅ Android Chrome 90+

## 📱 レスポンシブ対応

- **Desktop**: 1200px以上（2列レイアウト）
- **Tablet**: 768px-1199px（適応レイアウト）
- **Mobile**: 767px以下（1列レイアウト）

## ⚠️ 注意事項

- 表示料金は目安です（追加サービス料金別）
- Amazon商品情報は実際と異なる場合があります
- 配送は基本ECMS、対象外商品はFedX
- 関税は別途発生します

## 🔗 関連リンク

- [委託不可商品詳細](https://www.ecmsglobal-jp.com/cautions2)
- [関税率一覧](https://hts.usitc.gov/?utm_source=chatgpt.com)

## 📝 ライセンス

MIT License - 詳細は [LICENSE](LICENSE) ファイルを参照

## 🤝 コントリビューション

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)  
5. Open a Pull Request

## 📞 サポート

技術的なお問い合わせやバグ報告は、GitHub Issues をご利用ください。

---

**Powered by USDS × 十八願物流**