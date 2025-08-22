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
