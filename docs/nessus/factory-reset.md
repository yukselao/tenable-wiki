# Lisans Kaynaklı Erişim Sorunlarında Nessus'u Fabrika Ayarlarına Sıfırlama

Tenable Nessus Scanner'ın web arayüzüne lisans sorunları nedeniyle
erişemediğiniz durumlarda — örneğin aboneliğin süresi dolmuş ya da lisans
anahtarı yanlış yapılandırılmış olabilir — yeni lisans bilgilerini olağan
yolla girmek veya güncellemek mümkün olmayabilir. Bu gibi durumlarda
Nessus'u fabrika ayarlarına sıfırlamak; mevcut yapılandırmayı tamamen silip
yeni bir lisans kaydı yapmanın pratik bir çözümüdür.

Bu rehber Nessus kurulumunu sıfırdan başlatmak için izlemeniz gereken
adımları anlatır.

!!! danger "Veri kaybı uyarısı"
    Bu işlem; kullanıcı hesapları, tarama politikaları, tarama sonuçları ve
    diğer tüm Nessus verileri dahil **mevcut tüm yapılandırmayı siler**.
    İşleme başlamadan önce kritik bilgileri (örneğin scan policy export'ları,
    raporlar, custom plugin ayarları) **mutlaka yedekleyin**.

!!! note "Test ortamı"
    Aşağıdaki işlemler **Tenable Core üzerinde çalışan bir Nessus Scanner**
    üzerinde uygulanmıştır. Komut satırına (CLI) eriştikten sonra `sudo -i`
    komutuyla root yetkisi alınmış, ardından bu rehberdeki komutlar
    çalıştırılmıştır.

## Adım Adım Sıfırlama Süreci

Aşağıdaki komutları yetki yükseltilmiş halde (root veya `sudo`) çalıştırın.

### 1. Nessus servisini durdur

```bash
systemctl stop nessusd
```

### 2. Fabrika ayarlarına sıfırla

İki sıfırlama komutu sırayla çalıştırılır. İlki tüm yapılandırmayı,
ikincisi kalan kalıcı durumu temizler:

```bash
/opt/nessus/sbin/nessuscli fix --reset-all
/opt/nessus/sbin/nessuscli fix --reset
```

`--reset-all` kullanıcılar, politikalar, tarama sonuçları ve plugin
durumunu siler; `--reset` ise scanner kimliği dahil kalan konfigürasyonu
varsayılana çevirir. Komutlar interaktif onay isteyebilir; ekrandaki
talimatları izleyin.

### 3. Nessus servisini başlat

```bash
systemctl start nessusd
```

## Sıfırlama sonrası

Servis ayağa kalktıktan sonra web arayüzü (varsayılan TCP 8834) ilk kurulum
sihirbazını gösterir:

- Yeni admin kullanıcı adı ve parolası belirleyin.
- Yeni veya yenilenmiş **Activation Code** ile lisansı kaydedin.
- Plugin'lerin indirilmesini bekleyin (managed scanner ise SC tarafından
  push'lanır).

Servisin sağlıklı çalıştığını ve 8834 portunun dinlemede olduğunu doğrulamak
için:

```bash
systemctl status nessusd
ss -ltnp | grep 8834
```
