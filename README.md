- Nama : Nanda Amelia
- Nim  : 191402015

THE NAT CODE

- link youtube: https://youtu.be/V-l4xm8VOcE
- link ke-2 tutorial: https://docs.gns3.com/docs/using-gns3/advanced/the-nat-node/

     Node ini memungkinkan Anda untuk menghubungkan topologi ke internet melalui NAT. Node Internet tidak digunakan lagi untuk node ini, dan node Cloud. Node NAT memerlukan VM GNS3, atau komputer Linux dengan libvirt terinstal. Libvirt diperlukan, untuk membuat antarmuka virbr0 agar node ini berfungsi.
Secara default, node NAT menjalankan server DHCP dengan kumpulan yang telah ditentukan di kisaran 192.168.122.0/24.

1.	Buka https://www.gns3.com/marketplace/featured kemudian cari 

![1](https://user-images.githubusercontent.com/66839985/138512946-10b77a33-9328-42c2-854d-02661b75bcfc.png)

![2](https://user-images.githubusercontent.com/66839985/138512963-58d4ffe2-2817-49e8-a5da-503109d99bcd.png)

3.	Import aplikasi webtern tersebut

![3](https://user-images.githubusercontent.com/66839985/138512969-56444d64-eb6d-45c4-a7a7-0a12fab98aba.png)

![4](https://user-images.githubusercontent.com/66839985/138512972-75951b61-ab88-4588-856f-5c306e9acd54.png)

![5](https://user-images.githubusercontent.com/66839985/138512977-3c0a0966-ba82-4df9-b578-e5a596c12fa1.png)

4.	Tampilan saat webtern sudah diimport ke gns3

![6](https://user-images.githubusercontent.com/66839985/138513070-2dd02418-c316-4924-afd6-046fde75250e.png)

5.	Seret dan lepas NAT 

![7](https://user-images.githubusercontent.com/66839985/138598010-223b327f-3a9d-4b10-ab38-098787104de7.png)

6.	Seret dan lepas webtrem

![8](https://user-images.githubusercontent.com/66839985/138598015-9782ee25-952f-4841-98bf-bc94ab2f727d.png)

7.	Seret dan lepas Switch 1

![9](https://user-images.githubusercontent.com/66839985/138598019-2cdf4618-e010-4001-92ee-536255fa1a25.png)

8.	Hubungkan switch1 ke NAT dan Switch 1 ke webterm 1

![10](https://user-images.githubusercontent.com/66839985/138598023-a7a8416a-9fb5-4c0b-a709-9524294455d7.png)

![11](https://user-images.githubusercontent.com/66839985/138598025-67e7e964-e087-4cd5-9b4d-b0b7505265cf.png)

9.	Buka edit config

![12](https://user-images.githubusercontent.com/66839985/138598028-f47ecb16-f668-4259-9b09-07d976acb0f6.png)

10.	Untuk mengkonfigurasi wadah ini untuk menggunakan DHCP, batalkan komentar pada dua baris yang ditunjukkan pada gambar di bawah ini, dan klik Simpan

![13](https://user-images.githubusercontent.com/66839985/138598033-ab04eeec-0174-43c9-9bb2-e7d35b313703.png)

11.	Kemudian klik start

![14](https://user-images.githubusercontent.com/66839985/138598036-dba776e1-ed87-4a1f-9517-4f1ee2021471.png)

12.	Menggunakan perintah 'ifconfig' di terminal akan menunjukkan bahwa DHCP yang berjalan pada node NAT memberi wadah ini alamat 192.168.122.200 dari kumpulannya

![15](https://user-images.githubusercontent.com/66839985/138598039-f8221bba-6868-4e18-b202-add02866e256.png)

13.	Hentikan wadah Webterm, klik kanan, dan pilih "Edit konfigurasi" lagi. Kali ini, Anda akan mengomentari dua baris untuk DHCP, dan menghapus komentar pada baris di bagian Static IP dari file /etc/network/interfaces

![16](https://user-images.githubusercontent.com/66839985/138598040-bb2cc3fe-1837-47e7-bc17-6ba1c617ca22.png)

14.	Membuka terminal dan menjalankan "ifconfig" akan menunjukkan bahwa wadah menggunakan alamat IP yang ditetapkan secara statis

![17](https://user-images.githubusercontent.com/66839985/138598041-e1cbba23-5db8-4c8b-8fd1-9ff4ef699101.png)

15.	Memasukkan URL di bilah alamat Firefox akan membuka situs web

![18](https://user-images.githubusercontent.com/66839985/138598043-57677405-f705-4efa-bcb2-919a89046fd7.png)
