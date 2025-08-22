#!/bin/bash

# Top Komutu
Top komutu Linux sistemlerinde en temel ve sık kullanılan sistem izleme araçlarından biridir. Bu komut sayesinde sistemde çalışan tüm süreçleri görebilir, her sürecin CPU ve RAM kullanımını, kullanıcı bilgisini ve süreç ID’sini (PID) öğrenebilirsiniz. Top, sürekli güncellenen bir liste sunar; yani sistemi gözlemlerken bilgiler gerçek zamanlı olarak değişir. Top ekranında ayrıca süreçleri CPU veya bellek kullanımına göre sıralayabilir, sistem yükünü takip edebilir ve hangi uygulamanın daha fazla kaynak tükettiğini görebilirsiniz. Sistem yöneticileri ve geliştiriciler için performans analizi ve sorun tespiti açısından son derece önemlidir. Top komutunun bazı önemli özellikleri şunlardır:  
- Shift + P ile CPU kullanımına göre sıralama,  
- Shift + M ile RAM kullanımına göre sıralama,  
- q ile top’tan çıkış.  

bash -c "top -b -n 1 | head -n 20"

# Paket Yönetimi ve htop
Linux üzerinde yazılım ve araç yönetimi için paket yöneticileri kullanılır. Debian ve Ubuntu tabanlı sistemlerde apt paket yöneticisi yaygın olarak tercih edilir. Paket yönetimi iki temel adımdan oluşur: öncelikle sistemdeki paket listelerini güncellemek ve ardından ihtiyaç duyulan yazılımları yüklemek. Örneğin, htop, top komutuna göre daha modern, görsel ve interaktif bir süreç izleme aracıdır. Htop ile CPU ve RAM kullanımı, süreçler ve çekirdekler çok daha anlaşılır bir biçimde sunulur. Htop ayrıca süreçleri arama ve filtreleme imkânı sağlar, kullanıcılar süreçleri seçip menü üzerinden kolayca sonlandırabilirler. Bu araç özellikle çok çekirdekli sistemlerde CPU kullanımını grafik olarak göstermek için idealdir.  

bash -c "sudo apt update"
bash -c "sudo apt install -y htop"

# htop Kullanımı
Htop, top komutunun interaktif bir versiyonudur ve kullanıcı dostu bir arayüz sağlar. Renkli grafikler, süreçlerin ve kaynak kullanımının daha kolay okunmasını sağlar. Htop ile sistemdeki tüm süreçleri görebilir, CPU ve RAM kullanımını detaylı olarak inceleyebilir ve gereksiz süreçleri hızlıca sonlandırabilirsiniz. Fare ve klavye kısayolları ile filtreleme, arama ve süreç sıralama işlemleri kolayca yapılabilir. Örneğin, bir web tarayıcısı çok fazla RAM kullanıyorsa bunu kolayca tespit edip kapatabilirsiniz. Htop kullanmanın avantajları şunlardır:  
- Tüm süreçleri tek bakışta görebilme,  
- Kaynak kullanımına göre sıralama,  
- Arama ve filtreleme,  
- Menü üzerinden hızlı süreç sonlandırma.  

bash -c "htop"

# kill ve killall Komutları
Bazen Linux sistemlerde bazı süreçler takılabilir veya yanıt vermeyebilir. Böyle durumlarda süreçleri sonlandırmak gerekir. Kill komutu, belirli bir süreç ID’si (PID) verildiğinde sadece o süreci sonlandırır. Örneğin, bir program takıldığında PID ile kill komutu kullanılabilir. Killall komutu ise süreç ismi üzerinden çalışır ve o isimdeki tüm süreçleri kapatır. Ayrıca kill -9 PID komutu, süreci zorla sonlandırmak için kullanılır; bu, normal kill komutunun işe yaramadığı durumlarda gerekli olabilir. Bu komutlar sistemin sağlıklı çalışması ve takılan uygulamaların kapatılması için kritik öneme sahiptir.  

bash -c "kill 1234"
bash -c "killall firefox"

# ps Komutu
Ps komutu, sistemdeki süreçleri listelemek ve incelemek için kullanılan bir temel araçtır. Ps aux komutu ile kullanıcı bilgisi, PID, CPU ve RAM kullanımı gibi detaylı bilgiler elde edilebilir. Ps -ef komutu, farklı bir formatta süreçleri listeler ve genellikle yönetimsel işler için tercih edilir. Ps komutu grep ile birlikte kullanıldığında, belirli süreçleri aramak ve detaylı incelemek mümkündür. Örneğin, ps aux | grep firefox komutu, Firefox ile ilgili tüm süreçleri listeler ve hangi kaynakları kullandığını gösterir. Ps komutu sayesinde sistem yöneticileri hangi süreçlerin çalıştığını, ne kadar kaynak tükettiğini ve olası sorunları hızlıca tespit edebilirler.  

bash -c "ps aux"
bash -c "ps -ef"
bash -c "ps aux | grep firefox"
