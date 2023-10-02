# gl-matrix

Nama: Gabriella Natasya Br Ginting

NRP: 5025211081

Kelas: Grafika Komputer A

### Dokumentasi

- [Tugas 1](#tugas-1)
- [Tugas 2](#tugas-2)

## Tugas 1

Membuat 2D graphics bentuk persegi dari bentuk segitiga yang sudah dibuat sebelumnya.

**Code :**

- Menambahkan koordinat baru untuk agar terbentuk persegi

```
let  coords = new Float32Array( [ -0.5,-0.5, 0.5,-0.5, -0.5,0.5, 0.5,0.5 ] );
```

- Menyesuaikan warna pada persegi
```
/* Set up values for the "color" attribute */
   
let  color = new Float32Array( [ 0,1,0, 1,1,1, 0,0,1, 1,0,0 ] );
```

- Menggunakan `TRIANGLE_STRIP` agar tidak perlu menggambar ulang bentuk segitiga baru
```
/* Draw the square using TRIANGLE_STRIP. */
   
gl.drawArrays(gl.TRIANGLE_STRIP, 0, 4);
```

**Hasil :**


![tugas 1](/Images/triangle_strip.jpg)

## Tugas 2

Membuat 3D graphics bentuk kubus dan menampilkannya dari berbagai sudut pandang.

**Code :**

- Menampilkan dari bagian depan, arah kiri bawah.
```
drawPrimitive( gl.TRIANGLE_FAN, [0,1,0,1], [ -0.3,-0.3,-0.5, -0.3,0.7,-0.5, 0.7,0.7,-0.5, 0.7,-0.3,-0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [1,0,0,1], [ -0.5,-0.5,0.5, 0.5,-0.5,0.5, 0.5,0.5,0.5, -0.5,0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [0,0,1,1], [ -0.3,0.7,-0.5, -0.5,0.5,0.5, 0.5,0.5,0.5, 0.7,0.7,-0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [1,1,0,1], [ -0.3,-0.3,-0.5, 0.7,-0.3,-0.5, 0.5,-0.5,0.5, -0.5,-0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [1,0,1,1], [ 0.7,-0.3,-0.5, 0.7,0.7,-0.5, 0.5,0.5,0.5, 0.5,-0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [0,1,1,1], [ -0.3,-0.3,-0.5, -0.5,-0.5,0.5, -0.5,0.5,0.5, -0.3,0.7,-0.5 ]);
```

**Hasil :**

![tugas 2](/Images/front,left.jpg)

- Menampilkan dari bagian depan, arah kanan atas.
```
drawPrimitive( gl.TRIANGLE_FAN, [0,1,0,1], [ -0.7,-0.7,-0.5, -0.7,0.3,-0.5, 0.3,0.3,-0.5, 0.3,-0.7,-0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [1,0,0,1], [ -0.5,-0.5,0.5, 0.5,-0.5,0.5, 0.5,0.5,0.5, -0.5,0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [0,0,1,1], [ -0.7,0.3,-0.5, -0.5,0.5,0.5, 0.5,0.5,0.5, 0.3,0.3,-0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [1,1,0,1], [ -0.7,-0.7,-0.5, 0.3,-0.7,-0.5, 0.5,-0.5,0.5, -0.5,-0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [1,0,1,1], [ 0.3,-0.7,-0.5, 0.3,0.3,-0.5, 0.5,0.5,0.5, 0.5,-0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [0,1,1,1], [ -0.7,-0.7,-0.5, -0.5,-0.5,0.5, -0.5,0.5,0.5, -0.7,0.3,-0.5 ]);
```

**Hasil :**

![tugas 2](/Images/front,right.jpg)

- Menampilkan dari bagian belakang.
```
drawPrimitive( gl.TRIANGLE_FAN, [1,0,0,1], [ -0.5,-0.5,-0.5, -0.5,0.5,-0.5, 0.5,0.5,-0.5, 0.5,-0.5,-0.5 ]); // yang tampak
drawPrimitive( gl.TRIANGLE_FAN, [0,1,0,1], [ -0.5,-0.5,0.5, 0.5,-0.5,0.5, 0.5,0.5,0.5, -0.5,0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [0,0,1,1], [ -0.5,0.5,-0.5, -0.5,0.5,0.5, 0.5,0.5,0.5, 0.5,0.5,-0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [1,1,0,1], [ -0.5,-0.5,-0.5, 0.5,-0.5,-0.5, 0.5,-0.5,0.5, -0.5,-0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [0,1,1,1], [ 0.5,-0.5,-0.5, 0.5,0.5,-0.5, 0.5,0.5,0.5, 0.5,-0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [1,0,1,1], [ -0.5,-0.5,-0.5, -0.5,-0.5,0.5, -0.5,0.5,0.5, -0.5,0.5,-0.5 ]);
```

**Hasil :**

![tugas 2](/Images/back.jpg)

- Menampilkan dari bagian belakang, arah kiri bawah.
```
drawPrimitive( gl.TRIANGLE_FAN, [1,0,0,1], [ -0.3,-0.3,-0.5, -0.3,0.7,-0.5, 0.7,0.7,-0.5, 0.7,-0.3,-0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [0,1,0,1], [ -0.5,-0.5,0.5, 0.5,-0.5,0.5, 0.5,0.5,0.5, -0.5,0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [0,0,1,1], [ -0.3,0.7,-0.5, -0.5,0.5,0.5, 0.5,0.5,0.5, 0.7,0.7,-0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [1,1,0,1], [ -0.3,-0.3,-0.5, 0.7,-0.3,-0.5, 0.5,-0.5,0.5, -0.5,-0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [0,1,1,1], [ 0.7,-0.3,-0.5, 0.7,0.7,-0.5, 0.5,0.5,0.5, 0.5,-0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [1,0,1,1], [ -0.3,-0.3,-0.5, -0.5,-0.5,0.5, -0.5,0.5,0.5, -0.3,0.7,-0.5 ]);
```

**Hasil :**

![tugas 2](/Images/back,left.jpg)

- Menampilkan dari bagian belakang, arah kanan atas.
```
drawPrimitive( gl.TRIANGLE_FAN, [1,0,0,1], [ -0.7,-0.7,-0.5, -0.7,0.3,-0.5, 0.3,0.3,-0.5, 0.3,-0.7,-0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [0,1,0,1], [ -0.5,-0.5,0.5, 0.5,-0.5,0.5, 0.5,0.5,0.5, -0.5,0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [0,0,1,1], [ -0.7,0.3,-0.5, -0.5,0.5,0.5, 0.5,0.5,0.5, 0.3,0.3,-0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [1,1,0,1], [ -0.7,-0.7,-0.5, 0.3,-0.7,-0.5, 0.5,-0.5,0.5, -0.5,-0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [0,1,1,1], [ 0.3,-0.7,-0.5, 0.3,0.3,-0.5, 0.5,0.5,0.5, 0.5,-0.5,0.5 ]);
drawPrimitive( gl.TRIANGLE_FAN, [1,0,1,1], [ -0.7,-0.7,-0.5, -0.5,-0.5,0.5, -0.5,0.5,0.5, -0.7,0.3,-0.5 ]);
```

**Hasil :**

![tugas 2](/Images/back,right.jpg)