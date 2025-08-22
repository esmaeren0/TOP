Linux Süreç Yönetimi: top, htop, kill ve Paket Yönetimi

# Top Komutu: 
sistemde çalışan işlemleri gerçek zamanlı olarak gösterir.

# temel bileşenler: 

* PID: Process ID- Süreç kimlik numarası
* USER: Süreci çalıştıran kullanıcı
* %CPU: İşlemci kullanım yüzdesi
* %MEM: Bellek kullanım yüzdesi
* TIME+: Toplam işlemci kullanım süresi
* COMMAND: Çalıştırılan komut

 # Kısayollar:
* q: Çıkış
*k: işlem sonlandırma (PID girilir)
* Shift + P: CPU'ya göre sıralama
* Shift + M: Bellek kullanımına göre sıralama

# Sinyal Tipleri: 
 * SIGTERM (15): Kibarca sonlandırma (varsayılan)
 * SIGKILL (9): Zorla sonlandırma
```bash    
// Belirli bir PID'ye sahip süreci sonlandırma
kill -9 1234

// Belirli isimdeki tüm süreçleri sonlandırma
killall -9 firefox
```

# Ps komutu 
anlık olarak çalışan işlemler hakkında bilgi veirir.
sadece mevcut terminal oturumundaki işlemler listelenir. !!!

```bash 
ps //Mevcut terminaldeki süreçleri gösterir
ps aux // Tüm süreçleri detaylı gösterir 
```
* parametreler
  
| Seçenek | Açıklama |
|---------|----------|
| a       | Tüm kullanıcıların süreçlerini gösterir |
| u       | Kullanıcı bilgilerini ekler |
| x       | Terminale bağlı olmayan süreçleri gösterir |

# Htop komutu
kullanıcı dostu arayüz 
* htop komutu ile girilir. çıkış: F10
* F1: yardım 
* F2: yapılandırma
* F3:sonlandırma

  # Paket Yönetimi
  paket yöneticisi program kurma güncelleme kaldırma işlemlerini kolaylaştırır.
  * kurulum
    ```bash
    sudo apt install package_name
    ```
    
  * güncelleme
    ```bash 
    sudo apt update && sudo apt upgrade
      ```
  * kaldırma
    ```bash 
    sudo apt remove package_name
     ```
 
# dağıtıma göre paket yöneticileri

    - Ubuntu/Debian: apt veya dpkg
    - Fedora/Red Hat: dnf veya yum
    - Arch Linux: pacman
# Kill Komutu 

işlemi sonlandırma
   ```bash 
kill [sinyal] [PID]  // syntax
kill -15 1234
kill -SIGTERM 1234
  ```
