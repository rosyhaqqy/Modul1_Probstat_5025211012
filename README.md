### Praktikum 1 [ Probabilitas & Statistika ]
| Nama                      | NRP           |
|---------------------------|---------------|
|Moh rosy haqqy aminy       |5025211012     |

### Soal 1A 
```R
# 1.A
x <- 3
p <- 0.2
dgeom(x, p)
# hasil : [1] 0.1024
``` 
**Penjelasan**   

Fungsi `dgeom` adalah fungsi yang menerima parameter n dan peluang, akan didapatkan nilai peluang untuk bertemu 3 orang yang tidak menghadiri acara vaksinasi dan akan bertemu keberhasilan pertama dengan peluang 0.2.

**Screenshot**  

![1A](https://user-images.githubusercontent.com/86828535/194808121-cb3a300d-fade-4f07-b4b8-d41894a27280.png)

### Soal 1B  
**Kode Program**  
```R
# 1.B
data <- 10000
p <- 0.2
x <- 3
mean((rgeom(data, p) == x))
# hasil : [1] 0.10014
```  
**Penjelasan**  

fungsi `rgeom` adalah fungsi yang berguna untuk mendapatkan distribusi geometrik dengan variabel acak. Dalam hal ini, variabel acak sejumlah 10000 data dan peluangnya sebesar 0.2.

**Screenshot**  

![Screenshot 2022-10-10 133650](https://user-images.githubusercontent.com/86828535/194808832-ece82eb9-a52d-438f-8aa0-a8caaf046435.png)

### Soal 1C  
**Penjelasan**  

Pada poin a nilainya statis/tetap. sedangkan Pada poin b nilainya dinamis, tetapi mendekati nilai A. Sehingga dapat ditarik kesimpulan bahwa b menggunakan fungsi random, maka tentu hasilnya berbeda beda tetapi nilai poin b selalu mendekati poin a

### Soal 1D
**Kode Program**  
```R
# 1.D
data <- 10000
p <- 0.2
hist(rgeom(data, p), main = "Distribusi Geometrik Peluang X = 3 gagal sebelum sukses pertama")
```  

**Screenshot**  

![asnjdjdjej](https://user-images.githubusercontent.com/86828535/194809368-c2f98777-32bf-4505-a27a-2033482e1bd7.png)

### Soal 1E
**Kode Program**  
```R
# 1.E
p <- 0.2
q <- 1 - p
mean <- 1 / p
variance <- (q / (p^2))
mean
variance
# hasil : [1] 5
# hasil : [1] 20
```  

**Penjelasan**  

rumus `mean = 1/P` dan rumus `varians = Q/P^2`.

**Screenshot**

![Screenshot 2022-10-10 134607](https://user-images.githubusercontent.com/86828535/194809770-baea7419-8ff7-4519-a2a4-ed1c618dde18.png)

### Soal 2A
**Kode Program**  
```R
# 2.A
n <- 20
x <- 4
p <- 0.2
dbinom(x, n, p)
# hasil : [1]  0.2181994
```  
**Penjelasan**  

menggunakan fungsi `dbinom`

**Screenshot**

![Screenshot 2022-10-10 135310](https://user-images.githubusercontent.com/86828535/194810554-3fa6ca67-eec6-4445-8b9c-0667fb48bd79.png)

### Soal 2B 
**Kode Program**  
```R
# 2.B
x <- 10000
n <- 20
p <- 0.2
y <- rbinom(x, n, p)
hist(y, main = "Grafik Histogram Distribusi Binomial")
``` 
**Screenshot**

![sdsdnsjncsn](https://user-images.githubusercontent.com/86828535/194810770-b4326dc8-b52d-476d-b3fb-bda57a14dc9f.png)

### Soal 2C  
**Kode Program**  
```R
# 2.C
p <- 0.2
q <- 1 - p
n <- 20
mean <- n * p
variance <- n * p * q
mean
variance
# hasil : [1] 4
# hasil : [1] 3.2
``` 

**Penjelasan**  

rumus `mean = N*P` dan rumus `varians = N*P*Q`.  

**Screenshot**

![Screenshot 2022-10-10 135843](https://user-images.githubusercontent.com/86828535/194811284-70a8c500-9e2c-4352-998d-ade798eec9ce.png)

### Soal 3A  
**Kode Program**  
```R
# 3.A
lambda <- 4.5
x <- 6
dpois(x, lambda)
# hasil : [1] 0.1281201
```  

**Penjelasan** 

memanfaatkan fungsi `dpois`

**Screenshot**

![Screenshot 2022-10-10 140136](https://user-images.githubusercontent.com/86828535/194811666-d96ceff8-bf49-4ced-bd8e-e4a1a10492a7.png)

### Soal 3B  
**Kode Program**  
```R
# 3.B
lambda <- 4.5
n <- 365
hist(rpois(n, lambda), main = "Grafik histogram distribusi poisson kelahiran 6 bayi selama 1 tahun")
a <- (rpois(n, lambda) == 6)
mean(a)
# hasil : [1] 0.1260274
```  

**Screenshot**

![sjddsjbd](https://user-images.githubusercontent.com/86828535/194811909-aebe2edb-06d9-487d-82a3-972a027cf964.png)

### Soal 3C   
**Penjelasan** 

Pada poin a nilainya statis. Pada poin b nilainya dinamis, tetapi mendekati nilai a.

### Soal 3D 
**Kode Program**  
```R
# 3.D
lambda <- 4.5
mean <- lambda
variance <- mean
mean
variance
# hasil : [1] 4.5
# hasil : [1] 4.5
```  

**Penjelasan** 

rumus `mean = lambda` dan nilai varian didapatkan dengan cara `varian = mean`

**Screenshot**

![Screenshot 2022-10-10 141041](https://user-images.githubusercontent.com/86828535/194813116-35a7207b-f3f5-492f-a393-ff7340526f5b.png)

### Soal 4A  
**Kode Program**  
```R
# 4.A
x <- 2
v <- 10
dchisq(x, df = v)
# hasil : [1] 0.007664155
```  

**Penjelasan** 

menggunakan fungsi `dchisq`

**Screenshot**

![Screenshot 2022-10-10 141412](https://user-images.githubusercontent.com/86828535/194813545-86b19dc6-88ab-4aa0-b913-72d414ebccea.png)

### Soal 4B  
**Kode Program**  
```R
# 4.B
n <- 100
v <- 10
hist(rchisq(n, df = v), main = "Grafik Histogram Distribusi Chi-Square pada 100 Random Data")
```  

**Screenshot**

![kjfqkwh](https://user-images.githubusercontent.com/86828535/194813661-8bfbcfa1-4901-4168-a9b5-d28657e2aba2.png)

### Soal 4C  
**Kode Program**  
```R
# 4.C
v <- 10
mean <- v
variance <- v * 2
mean
variance
# hasil : [1] 10
# hasil : [1] 20
```  

**Penjelasan** 

rumus `mean = V` dan nilai varians didapatkan dengan cara `varians = 2*V`.

**Screenshot**

![Screenshot 2022-10-10 141656](https://user-images.githubusercontent.com/86828535/194813875-558579a9-9b52-4a5a-ae33-f005f8087d89.png)


### Soal 5A  
**Kode Program**  
```R
# 5.A
lambda <- 3
dexp(1, rate = lambda)
# hasil : [1] 0.1493612
```  

**Penjelasan** 

menggunakn fungsi `dexp`

**Screenshot**

![Screenshot 2022-10-10 142154](https://user-images.githubusercontent.com/86828535/194814532-357df3b2-8032-4c9e-8b1f-02d1ec5dc571.png)


### Soal 5B 
**Kode Program**  
```R
# 5.B
lambda <- 3
set.seed(1)
n_10 <- 10
hist(rexp(n_10, rate = lambda), main = "Histogram Distribusi Exponensial 10 Angka Acak")
set.seed(1)
n_100 <- 100
hist(rexp(n_100, rate = lambda), main = "Histogram Distribusi Exponensial 100 Angka Acak")
set.seed(1)
n_1000 <- 1000
hist(rexp(n_1000, rate = lambda), main = "Histogram Distribusi Exponensial 1000 Angka Acak")
set.seed(1)
n_10000 <- 10000
hist(rexp(n_10000, rate = lambda), main = "Histogram Distribusi Exponensial 10000 Angka Acak")
```   

**Screenshot**

10

![10](https://user-images.githubusercontent.com/86828535/194814866-f93b3f2f-759b-47c8-86b4-149153bd9eac.png)

100

![100](https://user-images.githubusercontent.com/86828535/194814892-cc3545ac-e0e1-4bcd-8794-9f4c102636d4.png)

1000

![1000](https://user-images.githubusercontent.com/86828535/194814912-71fa0981-7a4b-47ea-8e2d-44d78eebdeb1.png)

10000

![10000](https://user-images.githubusercontent.com/86828535/194814923-23110a03-c8b0-48fa-92f2-6bfc2624f39e.png)


### Soal 5C  
**Kode Program**  
```R
lambda <- 3
n <- 100
set.seed(1)
mean <- mean(rexp(n, rate = lambda))
variance <- (sd(rexp(n, rate = lambda)))^2
mean
variance
# hasil : [1] 0.3435588
# hasil : [1] 0.06560765
```  

**Penjelasan** 

menggunakan fungsi bawaan `mean` dan `variance`.

**Screenshot**

![Screenshot 2022-10-10 142705](https://user-images.githubusercontent.com/86828535/194815235-239caee9-0295-4aeb-b3a1-99f94215e0ac.png)

### Soal 6A  
**Kode Program**  
```R
# 6.A
n <- 100
mean <- 50
sd <- 8
data <- rnorm(n, mean, sd)
rata <- mean(data)
x1 <- floor(rata)
x2 <- ceiling(rata)
x1
x2
rata
z <- (data - rata) / sd(data)
plot(z, main = "Grafik Z-Score")
```  

**Penjelasan** 

mengunakan fungsi `rnorm` lalu akan di `floor` menjadi x1 dan di `ceiling` menjadi x2.

**Screenshot**

![Screenshot 2022-10-10 151836](https://user-images.githubusercontent.com/86828535/194822849-94b44f22-69a8-4527-b50d-3a7db4098870.png)

### Soal 6B  
**Kode Program**  
```R
# Soal 6B
n <- 100
mean <- 50
sd <- 8
data <- rnorm(n, mean, sd)
hist(data, 50, main = "5025211012_Moh Rosy Haqqy Aminy_Probstat_A_DNhistogram ")
```  

**Screenshot**

![jhfhj](https://user-images.githubusercontent.com/86828535/194823012-2aeb10e5-610b-418e-8b4f-ee425cc057ac.png)

### Soal 6C  
**Kode Program**  
```R
# Soal 6C
n <- 100
mean <- 50
sd <- 8
data <- rnorm(n, mean, sd)
sdd <- sd(data)
variance <- sdd * sdd
variance
```  

**Penjelasan** 

nilai varians pada distribusi normal dapat diketahui dengan kuadrat dari standar deviasi  

**Screenshot**

![Screenshot 2022-10-10 152138](https://user-images.githubusercontent.com/86828535/194823282-3bffa325-2e26-4a97-81ea-953e636ddcc5.png)

-------
<p align="center"> 
  NO ROYAL ROAD IN GEOMETRY
</p>

