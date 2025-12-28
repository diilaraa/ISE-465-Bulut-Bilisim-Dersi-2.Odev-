## Kullanılan Komutlar

### 1. PowerShell Üzerinden EC2 Instance'ına Bağlantı
Öncelikle, anahtar dosyasının bulunduğu dizine geçilmiştir:
```powershell
cd C:\xx\xx
```

EC2 instance'ına SSH bağlantısı:
```bash
ssh -i portfolio-key.pem ec2-user@35.159.24.206
```

### 2. Sistem Güncellemesi
```bash
sudo dnf update -y
```

### 3. Apache HTTP Server Kurulumu

Apache HTTP Server kurulumu:
```bash
sudo dnf install httpd -y
```

Apache servisinin başlatılması:
```bash
sudo systemctl start httpd
```

Apache servisinin sistem başlangıcında otomatik çalışması için etkinleştirilmesi:
```bash
sudo systemctl enable httpd
```

### 4. SCP ile Portfolio Dosyalarının Sunucuya Aktarılması
```bash
scp -i portfolio-key.pem -r Portfolio ec2-user@PUBLICIP:/home/ec2-user/
```

### 5. Dosya Aktarımının Kontrol Edilmesi
```bash
ls
```

### 6. Web Dizininin Yapılandırılması

HTML dosyasının Apache web dizinine taşınması:
```bash
sudo mv Portfolio/DilaraTopPortfolio.html /var/www/html/index.html
```

Görsel dosyasının Apache web dizinine taşınması:
```bash
sudo mv Portfolio/profile.jpg /var/www/html/
```

### 7. Dosya Sahipliği ve Yetkilendirme Ayarları

Dosya sahipliğinin Apache kullanıcısına atanması:
```bash
sudo chown apache:apache /var/www/html/index.html /var/www/html/profile.jpg
```

Dosya izinlerinin ayarlanması:
```bash
sudo chmod 644 /var/www/html/index.html /var/www/html/profile.jpg
```
