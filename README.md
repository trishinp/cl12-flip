# 左右反転画像 生成プログラム flip.py
## 1. 概要
引数で指定した画像の左右反転画像を作成する python3で動作するプログラムです。
## 2. ソースコード

```python
# このプログラムは python3用です。
# あらかじめ pip install pillow で pillow をインストールしておきます。
from PIL import Image
import sys

# コマンド引数から入力画像と出力画像のファイル名を取得
input_image = sys.argv[1]
output_image = sys.argv[2]

# 画像の読み込み
img = Image.open(input_image)

# 画像の左右反転
img_flip = img.transpose(Image.FLIP_LEFT_RIGHT)

# 画像の保存
img_flip.save(output_image)
```
## 3. 使い方
### 3.1.実行例
 - コマンドラインフォーマット
   ```python
   python3 flip.py <input_image_path> <output_image_path>
   ```
 - 利用例
   ```python
   python3 flip.py input.jpg output.jpg
   ```
### 3.2.出力結果
 - 以下のように入力画像の左右反転画像が出力されます。
   
 <table width="100%">
  <tr>
    <th width="50%" align="center">入力画像(input.jpg)</th>
    <th width="50%" align="center">出力画像(output.jpg)</th>
  </tr>
  <tr>
    <td align="center">
      <img width="95%" alt="input" src="https://github.com/user-attachments/assets/1d1add63-efba-4545-9b6d-0da6b21d1c21" />
    </td>
    <td align="center">
      <img width="95%" alt="output" src="https://github.com/user-attachments/assets/5de253cd-6e02-41c8-94ac-6304ced8619b" />
    </td>
  </tr>
</table>


以上
   
