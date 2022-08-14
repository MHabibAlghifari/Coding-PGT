<h2> Cara Berkolaborasi di GitHub </h2>
<h3> Alur Kerja Tarik-Permintaan untuk Kontribusi Kode </h3> 
Alur kerja untuk mengkontribusikan kode dapat terasa menakutkan pada awalnya. Yang paling penting untuk diingat adalah mengikuti pola dan standar yang digariskan oleh proyek yang sedang Anda kerjakan (seperti yang telah kita diskusikan). Alur kerja umum yang didukung oleh GitHub cukup sederhana.

1. Fork target repo ke akun Anda sendiri.
2. Klon repo ke mesin lokal Anda.
3. Lihat "cabang topik" baru dan buat perubahan.
4. Dorong cabang topik Anda ke garpu Anda.
5. Gunakan penampil diff pada GitHub untuk membuat permintaan tarik melalui diskusi.
6. Lakukan perubahan apa pun yang diminta.
7. Permintaan tarik kemudian digabungkan (biasanya ke dalam cabang master) dan cabang topik dihapus dari repo hulu (target).

<h4> Langkah 1: Forking </h4> 

![github_header](https://user-images.githubusercontent.com/111033936/184522675-eb90c033-3bb9-4df2-959f-b7826d4cddbd.png)

<h4> Langkah 2: Cloning </h4> 
Clone repo menggunakan URL di sidebar kanan:

![clone_url](https://user-images.githubusercontent.com/111033936/184522715-d37a6c13-d21b-4535-87d2-dc0e07c319e1.png)

<h4> Langkah 3: Menambahkan Remote Hulu </h4>
Ubah ke direktori kloning dan kemudian pada titik ini, Anda dapat menambahkan remote hulu:

cd jquery
git remote add upstream git@github.com:jquery/jquery.git

git fetch upstream
git merge upstream/master

<h4> Langkah 4: Memeriksa Cabang Topik </h4> 
Namun, sebelum Anda membuat perubahan sendiri, periksa cabang topik:

git checkout -b enhancement_345

<h4> Langkah 5: Berkomitmen </h4> 
membuat perubahan, dan membuat komit yang hanya melacak perubahan tersebut.

git commit -am "adding a smileyface to the documentation."

<h4> Langkah 6: Mendorong </h4> 
mendorong cabang topik ini ke fork proyek Anda sendiri.

git push origin enhancment_345

<h4> Langkah 7: Membuat Permintaan Tarikn </h4>

khirnya, Anda akan membuat permintaan tarik. Pertama, pergi ke fork repo Anda. Anda mungkin melihat "cabang yang baru saja didorong", dan jika demikian, Anda dapat memilih "Bandingkan dan Tarik Permintaan". Jika tidak, Anda dapat memilih cabang Anda dari dropdown, dan kemudian klik "Pull Request" atau "Compare" di kanan atas bagian repo.

![compare_pull_request](https://user-images.githubusercontent.com/111033936/184522827-fa1cd0d6-3151-439c-b31f-a1e6af075ef1.png)

compare_pull_request
Membuat permintaan tarik melalui tombol Compare and Pull Request.

![switch_branches](https://user-images.githubusercontent.com/111033936/184522836-a6f4a47f-c224-46a3-a8b6-8876cee94084.png)








