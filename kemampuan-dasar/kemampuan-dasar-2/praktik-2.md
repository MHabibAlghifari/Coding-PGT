<h2> Team Collaboration With GitHub </h2>
  <h3> Alat 1: Menambahkan Anggota Tim</h3>
  Biasanya ada dua cara menyiapkan Github untuk kolaborasi tim:
  
Organizations - Pemilik organisasi dapat membuat banyak tim dengan tingkat izin yang berbeda untuk berbagai repositori
Collaborators - Pemilik repositori dapat menambahkan kolaborator dengan akses Baca + Tulis untuk satu repositori

![github-team-create-org](https://user-images.githubusercontent.com/111033936/184522995-b24a2055-6883-423f-8821-344b4c1dbd6c.png)

Pull Only: Fetch and Merge dengan repositori lain atau salinan lokal. Akses hanya baca.
Push and Pull: (1) bersama dengan pembaruan reparasi jarak jauh. Baca + Akses tulis.
Push, Pull & Administrative: (1), (2) bersama dengan hak atas info penagihan, membuat tim serta membatalkan akun Organization. Baca + Tulis + akses Admin

![github-team-create-team](https://user-images.githubusercontent.com/111033936/184523005-7615e417-12b6-439f-8877-34e43d684737.png)

Collaborators
Collaborators digunakan untuk memberikan akses Read + Write access ke satu repositori yang dimiliki oleh akun pribadi. Untuk menambahkan Collaborators, (akun pribadi Github lainnya), cukup buka https://github.com/[username]/[repo-name]/settings/collaboration:

![github-team-collaborator](https://user-images.githubusercontent.com/111033936/184523026-8786968f-3fcc-4d88-b2b7-a74a69cebfed.png)

Collaborator kemudian akan melihat perubahan dalam status akses pada halaman repositori. Setelah kita memiliki akses Write ke repositori, kita dapat melakukan git clone, bekerja pada perubahan, membuat git pull untuk mengambil dan menggabungkan setiap perubahan dalam repositori jarak jauh dan akhirnya git push, untuk memperbarui repositori jarak jauh dengan perubahan kita sendiri:

![github-team-access](https://user-images.githubusercontent.com/111033936/184523035-15b06c9d-ddc4-4f24-b9fb-dae79fae7e78.png)

  <h3>Alat 2: Pull Requests </h3>
  
  Fork & Pull Model - Digunakan di repositori publik yang tidak memiliki akses push
Share Repository Model - Digunakan dalam repositori pribadi yang kita miliki akses push. Fork tidak diperlukan adalah case ini.

1. Identifikasi Github Repository yang ingin Anda kontribusikan, dan klik tombol "Fork" untuk membuat tiruan dari repositori di akun Github Anda sendiri:

![github-team-fork](https://user-images.githubusercontent.com/111033936/184523140-f7711c14-c099-4daf-b768-849271e19613.png)

2. Ini akan membuat salinan persis dari repositori di akun Anda sendiri

![github-team-forked](https://user-images.githubusercontent.com/111033936/184523147-09a101b6-5bac-463c-89a7-8d4f9d7a5055.png)

3. Pilih URL SSH sehingga akan meminta kata kunci SSH Anda, bukan nama pengguna dan kata sandi setiap kali Anda git push atau git pull. Selanjutnya, kita akan mengkloning repositori ini ke komputer lokal:

$ git clone [ssh-url] [folder-name]
$ cd [folder-name]

4. Pilih URL SSH sehingga akan meminta kata kunci SSH Anda, bukan nama pengguna dan kata sandi setiap kali Anda git push atau git pull. Selanjutnya, kita akan mengkloning repositori ini ke komputer lokal:

$ git clone [ssh-url] [folder-name]
$ cd [folder-name]

5. Setelah membuat penambahan yang relevan untuk membangun fitur-fitur baru, kita hanya akan melakukan perubahan baru dan checkout ke git master branch:

$ git add .
$ git commit -m "information added in readme"
$ git checkout master

6. Pada titik ini, kita akan mendorong cabang ke repositori jarak jauh. Untuk ini kita akan memeriksa nama cabang dengan fitur baru serta alias git remote repository. Lalu kita akan mendorong perubahan menggunakan git push [git-remote-alias] [branch-name]:

$ git branch
* master
readme
$ git remote -v  

7. origin  git@github.com:[forked-repo-owner-username]/[repo-name].git (fetch)
origin  git@github.com:[forked-repo-owner-username]/[repo-name].git (push)
$ git push origin readme
Di halaman Github repositori bercabang, kita akan beralih ke cabang dengan fitur baru dan kemudian tekan tombol "Pull Request".

![github-team-pull-request](https://user-images.githubusercontent.com/111033936/184523238-d94ad635-3395-4b17-a0dc-0104ca8e3702.png)

8. Setelah mengirimkan pull request, itu akan langsung membawa kita ke halaman pull request repositori asli. Kita akan melihat pull request, baik sebagai masalah baru maupun pull request baru.

![github-team-pull-request-sent](https://user-images.githubusercontent.com/111033936/184523249-4c96a80c-9627-4fa2-993f-92e9e7c7acb1.png)

9. Setelah diskusi, mungkin pemilik repositori bercabang mungkin ingin menambahkan perubahan pada fitur baru. Dalam hal ini, kita akan melakukan pembayaran ke cabang yang sama di komputer lokal, menjalankannya, dan mendorongnya kembali ke Github. Ketika kita mengunjungi halaman pull request dari repositori asli, itu akan secara otomatis diperbarui!

![github-team-pull-request-2](https://user-images.githubusercontent.com/111033936/184523258-3a710b67-26c5-46a7-8951-6712d198126d.png)
![github-team-merge](https://user-images.githubusercontent.com/111033936/184523288-ac7d8d92-5878-470d-b10e-39fc2ec2d6c3.png)

<h2> Penggabungan Pull Request </h2>

![github-team-merge](https://user-images.githubusercontent.com/111033936/184523290-1392b4de-a8c3-4159-aa5d-b1eb724ccf4a.png)

![github-team-merge-conflict](https://user-images.githubusercontent.com/111033936/184523293-2352fd57-5e55-4278-ab21-f2d6cdf55321.png)










