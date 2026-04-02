Part A — Concept Check

Why does a linked list need a head variable?

Why does each node store a next reference?

Why is insertion at the beginning easier in linked list than in array?

Part B — Code Reading

In insertAtBeginning(), why do we write: newNode.next = head; head = newNode; in that order?

In display(), what would happen if we accidentally wrote: while (current.next != null) instead of: while (current != null)

Part C — Comparison with Array

Which structure is better for fast random access?

Which structure is better for frequent insertion at the beginning?

Why does linked list use more memory than array?

Jawaban:

PART A:
-Butuh head dikarenakan linked list ini tidak punya indeks. Jadi head yang jadi pintu masuk nya kita.
-Next dibutuhkan untuk jadi semacam peta dimalam lokasi node di memori. Pengarah yang memberitahu dimana data disimpan.  
-insert diawal mudah dikarenakan tidak adanya shifting dan kita hanya mengubah dua referensi pointer.  

PART B:
-Urutan ini wajib supaya kita tidak kehilangan alamat data yang sudah ada. Kita sambungkan dulu node baru ke list yang lama, baru setelah aman, kita pindahkan label head ke node yang baru tersebut.
-current.next != null akan berhenti di node terakhir. Jika digunakan untuk display(), data di node terakhir tidak akan tercetak karena loop berhenti sebelum memproses datanya.

PART C:
-Karena Array menggunakan alamat memori yang berdekatan, kita bisa langsung melompat ke alamat tertentu menggunakan rumus matematika $(base\_address + index \times size)
-Cukup mengubah pointer, selesai O(1).
-Selain menyimpan data (misal int), Linked List harus menyimpan referensi next (pointer) untuk setiap node. Array hanya menyimpan data murni.
