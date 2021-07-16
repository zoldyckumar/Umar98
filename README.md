# image-processing
UAS
# Python scripts untuk gambar transformations

![img.png](example-imgs/img.png) (img.png)

## Setup
Pastikan python diinstal dan diinstal dengan benar [Pillow](https://pillow.readthedocs.io/)

    $ pip install Pillow

## opacity.py
Mengubah opacity gambar dengan mengalikan saluran alfa setiap piksel untuk nilai yang ditentukan.

contoh:

    $ python opacity.py img.png 0.4

![img_opacity_0.4.png](example-imgs/img_opacity_0.4.png) (img_opacity_0.4.png)

## tint.py
Mengubah warna gambar ke nilai RGB yang ditentukan dengan menjaga alfa tidak berubah.

Contoh:

    $ python tint.py img_opacity_0.4.png 10 20 200

![img_opacity_0.4_tinted.png](example-imgs/img_opacity_0.4_tinted.png) (img_opacity_0.4_tinted.png)

## negative.py
Mengubah warna gambar menjadi negatif, alfa tidak berubah.

Contoh:

    $ python negative.py img_opacity_0.4_tinted.png

![img_opacity_0.4_tinted_negative.png](example-imgs/img_opacity_0.4_tinted_negative.png) (img_opacity_0.4_tinted_negative.png)

## invert.py
Membalikkan opacity gambar.
Contoh:

    $ python invert.py img_opacity_0.4_tinted.png

![img_opacity_0.4_tinted_inverted.png](example-imgs/img_opacity_0.4_tinted_inverted.png) (img_opacity_0.4_tinted_inverted.png)

    $ python invert.py img.png

![img_inverted.png](example-imgs/img_inverted.png) (img_inverted.png)

## white_to_transparent.py
Mengonversi piksel putih gambar menjadi piksel transparan

Contoh:

![img_white.png](example-imgs/img_white.png) (img_white.png)

    $ python white_to_transparent.py img_white.png

![img_white_transp.png](example-imgs/img_white_transp.png) (img_white_transp.png)

## Tips
Anda dapat memproses lebih banyak gambar secara bersamaan

Contoh:

Ubah opacity 'img.png' dan 'img2.png'

    $ python opacity.py img.png img2.png 0.4

Ubah opacity semua file png di folder 'ikon'

    $ python opacity.py icons/*.png 0.4
