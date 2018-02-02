# tutorial-for-designer
2018冬デザイナー向け体験講義資料

- UnityとAsset Storeの活用
- キャラクターの活用方法
- PBRの活用方法
- 公開方法

# 講義概要
- Unity体験 / Asset Storeを活用しよう
- 自作キャラクターをUnityで動かす手順
- GitHubで公開しよう

# 必要なアカウント
- Unity
- GitHub

# Unity体験 / Asset Storeを活用しよう
- サイトの紹介 https://unity3d.com/jp
- 起動
- Unityアカウントの作成
- 新しい3Dプロジェクトを作成
- Asset Storeでサンプルを確認
  - [RED PANDA. Sky City Lite](http://u3d.as/vPD)
    - CrossPlatformInputInitialize.csを消す

## Unity基本操作
- 基本操作
- カメラを固定にする
- Sun(Directional Light)でPBR体験 Xを0辺りにする
- FPS Controllerのコントローラーを無効にして動かなくして、位置を調整

## キャラクターの読み込み
- [unity-chan! "Unity-chan!" Model](https://assetstore.unity.com/publishers/7659)
- Actionシーン
- 表情とシーン切り替えメニューを消す
  - FaceUpdateスクリプトを無効にする
  - 2つのLevelUpdateオブジェクトを消す

# 自作キャラクターをUnityで動かす手順
今回は Sketchfab から素体を探して入れてみましょう。

- https://sketchfab.com/ を開く
- Modelsを選択して、FiltersのFETURESでDownloadableをチェック
- Characterで検索
  - Model Informationで容量などを確認。FBX推奨
  - 容量は、ダウンロード時に20倍ぐらいになるので注意
  - https://sketchfab.com/models/b5f1d7635a5b41f0847a2ee5b906098a

## MAYAでアニメーションの設定


## Unityで動かす
- Unityに読み込み
- Importerで以下をやってApply
  - カメラなどの不要なチェックをはずす
  - RigをHumanoidにする
- Unityちゃんの子供にする
- Unityちゃんのチェックをはずす
- Unityちゃんのルートのアニメーションのアバターを入れかえる(キャラクターについているAnimatorは設定不要)

# PBRの確認
- 新規にマテリアルを作成して、テクスチャーを設定
  - Normalをノーマルマップにして読み直し
- ライティングを設定して、焼き込む
- キャラクターを読み込む
  - Metaricにディテールを設定
- [Unity Technologies. Post Processing Stack]
- CameraのBloomの値を調整したり、外したりして、画面効果を確認する

# WebGL
- Edit -> Project Settings -> Qualityで、WebGLを最高クオリティに変更
- 学校でやる時は、GzipをDisableに変更

