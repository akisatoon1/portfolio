# 3D-model-TOKYO（都市再現3Dモデル）

## 概要
1m間隔の格子状標高値（電子地図データ）を解析し、東京ドーム周辺の都市街区を3Dモデルで再現するプロジェクトです。欠損値（標高値 -9999.99）を含む膨大な点群データから、建物と地表を判別して可視化しました。

## 構成図
### deploy
https://github.com/akisatoon1/3D-Model-TOKYO/blob/main/system/deploy.md
### ビルを生成
https://github.com/akisatoon1/3D-Model-TOKYO/blob/main/system/makeBuilding.md
### 点群のノイズを処理
https://github.com/akisatoon1/3D-Model-TOKYO/blob/main/system/opening.md

## イメージ
### イメージ画像複数
https://github.com/akisatoon1/3D-Model-TOKYO/tree/main/result/pictures 
### イメージ動画
https://www.youtube.com/watch?v=Kzt4w49KwOo

## 技術的工夫

- **建物判定とノイズ除去の最適化：** 点群データを地表と建物に分類する際、データの精度を向上させるため、画像処理のアルゴリズムを応用したノイズ除去処理を実装しました。
- **造形品質を向上させる独自アルゴリズム**：建物をより綺麗に表現するために、直方体で表現するという手法を採用しました。さらに、直方体とは大きく異なる形状の建物に対しては、直方体判定アルゴリズムを設計し、ありのままに3Dモデル化しました。これにより、リアルさと綺麗さを同時に実現しました。また、側面を追加したほうがリアルかつ綺麗であると考え、側面を追加する処理も加えました。
- **アルゴリズムの拡張：** 既存の手法では表現が不十分だった部分に対し、独自の追加処理を実装することで、モデルの見た目向上を図りました。
