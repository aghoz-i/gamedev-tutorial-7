# Tutorial 7
## Latihan mengikuti dokumen Tutorial
Disini, saya mengikuti dokumen tutorial dari awal hingga sebelum latihan mandiri.
Sejauh ini, tidak ada yang berbeda dari dokumen tutorial.
## Latihan Mandiri
### Implementasi Crouch dan Sprint

Implementasi crouch dan sprint yang ditambahkan hanya sekedar perubahan kecepatan player ketika ditekan tombol tertentu.
Ketika tombol CTRL ditekan, maka kecepatan player akan berkurang.
Sedangkan, ketika tombol SHIFT atau ALT ditekan, maka kecepatan player akan bertambah.

Implementasi ini dilakukan dengan mengalikan movement_vector, setelah dinormalisasi, dengan angka pengali.
Implementasi ini dilakukan dengan mengedit script `Player.gd`.
```
# Normalisasi kecepatan
movement_vector = movement_vector.normalized()
# jika tombol hotkey crouch ditekan, kali movement_vector dengan 0.7
if Input.is_action_pressed("crouch"):
  movement_vector *= 0.7
# sedangkan, jika tombol hotkey crouch sedang tidak ditekan, dan tombol sprint ditekan, kali movement_vector dengan 1.5
elif Input.is_action_pressed("sprint"):
  movement_vector *= 1.5
```

Selain itu, ditambahkan juga di project setting, input map untuk `crouch` dan `sprint`, dan hotkey untuk memicunya.

