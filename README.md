•••Pengenalan Algoritma
Algoritma dideskripsikan sebagai sekumpulan instruksi untuk menyelesaikan suatu tugas tertentu. 
Implementasi suatu algoritma tidak berguna jika tidak memahami atau membandingkan kelebihan dan kekurangan antar algoritma.

•••Logaritma
Logaritma merupakan kebalikan dari pemangkatan (eksponensial).

•••Binary Search
Binary search merupakan suatu algoritma dimana inputan dari algoritma adalah suatu list yang terdiri dari sebuah element yang terurut.
Binary Search hanya bisa digunakan ketika list yang dimiliki sudah terurut. Ketika element yang ingin dicari berada dalam list yang terurut tadi maka binary search akan mengembalikan posisi dari kata tersebut, tetapi jika kata tidak ditemukan maka binary search akan mengembalikan nilai null (kosong). 
Dengan menggunakan binary search selalu menebak angka diposisi tengah dan akan selalu mengeliminasi setengah dari jumlah angka yang tersisa setiap kali melakukan tebakan. 
Binary Search membutuhkan sejumlah log n operation untuk memeriksa list dengan ukuran n oleh karenanya running time untuk binary search ketika diekspresikan dengan violation adalah O log n. Binary Search akan menerapkan logaritmik time atau lock time.

•••Performa Binary Search vs Simple Search 
Mencari suatu kata dalam suatu dictionary yang di dalam dictionary tersebut terdapat 240.000 kata. Berapa banyak tahapan atau langkah yang perlu dilakukan ketika menggunakan simple search dan ketika menggunakan binary search. 
Jika menggunakan Simple Search maka jumlah tahapan terbanyak yang mungkin dilakukan ialah 240.000 tahapan, jika kata yang ingin dicari berada pada bagian akhir dictionary. 
Dibandingkan dengan binary search untuk kondisi terburuk binary search hanya membutuhkan 18 tahapan karena di setiap kali tebakan binary search sudah mengeliminasi sejumlah setengah dari total jumlah kata di dalam dictionary. Simple Search menerapkan linear time dan binary search menerapkan logaritmik time.

•••Big O Notation
Big O Notation merupakan spesial notation atau notasi khusus yang bisa digunakan untuk mendeskripsikan seberapa cepat suatu algoritma.

•••Penerapan Big O Notation
Big O Notation mengekpresikan bagaimana kecepatan suatu algoritma. Big O Notation tidak mengekspresikan kecepatan suatu algoritma dalam satuan second atau detik, Big O Notation memungkinkan untuk membandingkan jumlah operasi dimana big o akan mengekspresikan bagaimana kecepatan suatu algoritma berkembang dari suatu algoritma.

•••5 Big O Notation yang umum ditemui 
1.	O(log n), juga dikenal dengan log time. 
Contoh: binary search
2.	O(n), juga dikenal dengan linear time. 
Contoh: simple search
3.	O(n * log n)
Contoh: quicksort
4.	O(n²) 
Contoh: selection sort
5.	O(n!) 
Contoh: traveling sales person problem

Implementasi Binary Search dengan Python
Terdapat suatu function yang bernama binary_search yang akan menerima dua parameter, pertama itu sorted array atau list yang sudah terurut dan kedua itu item yang akan dicari. 
Bila item yang dicari terdapat dalam list maka function akan mengembalikan posisi dari item tersebut di dalam list. Jumlah pengecekan maksimum atau jumlah tebakan maksimum akan sama dengan jumlah elemen yang terdapat dalam list yang diistilahkan sebagai linear time.


def binary_search(list, item):
    low = 0
    high = len(list)-1

    while low <= high:
        mid = (low+high)//2
        guess = list[mid]
        if guess == item:
            return mid
        if guess>item- 1 :
            high=mid -1
        else :
            low=mid+1
    return None

my_list = [1,3,5,7,9]
print (binary_search(my_list,3))# =>1




