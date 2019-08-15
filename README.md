# 北海道・札幌市オープンデータ
各種オープンデータを使った分析や可視化の事例

## 北海道警察　犯罪オープンデータ / HokkaidoPoliceCrimes

ひったくりや車上狙いなど，窃盗に関するデータを発生地の住所をジオコーティングによって経緯度座標を付加した．

生成した CSVを uberのオープンソース・ソフトウェア [Kepler.gl](https://kepler.gl/) によって地図上にプロット，分析を行った．

- [犯罪オープンデータの可視化例](https://tkhrmeme.github.io/HokkaidoOpendata/keplergl_crimes.html)

## 札幌市円山動物園　入場者数オープンデータ / MaruyamaZoo

[オリジナルデータ](./MaruyamaZoo/original_data/)には以下のような不具合？があったので[処理済みのデータ](./MaruyamaZoo/data/)を作成した．

- 2011年4月1日～2018年8月31日のデータ
  - カラム名が他のデータと違う
  - 2018/4/1の行だけ数値に桁区切りのカンマが入っている
- 2018年9月1日～2018年9月30日データ
  - 他はUTF-8だが，一つだけエンコードが Shift_JIS
  - カラム名「I:CのうちD～H以外」に含まれるチルダ～の文字コードが，他は0xff5eだが，一つだけ0x301c
- 2019年7月1日～2019年7月31日のデータ
  - 最後に余計な空行が残っている

jupyter nootbook形式のCSVファイルの読み込みやデータのプロットの[コード](./MaruyamaZoo/MaruyamaZoo.ipynb)
