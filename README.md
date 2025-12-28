# AWS EC2 Üzerinde Portfolio Web Sitesi Dağıtımı

Bu repository, Amazon Web Services (AWS) bulut altyapısı kullanılarak geliştirilen kişisel bir portfolio web sitesinin dağıtım sürecini belgelemek amacıyla hazırlanmıştır. Proje, bir web uygulamasının bulut ortamında nasıl kurulacağı, yapılandırılacağı ve yayınlanacağı adım adım ele alınmıştır.

## Projenin Amacı

Bu projenin temel amacı, bulut bilişim altyapılarının sunduğu olanakları uygulamalı olarak deneyimlemek ve gerçek bir web uygulamasını AWS ortamında dağıtmaktır. Bu kapsamda, sanal sunucu oluşturma, ağ ve güvenlik yapılandırmaları, depolama yönetimi, uzaktan bağlantı sağlama ve dosya aktarımı gibi temel bulut bilişim kavramları pratik olarak uygulanmıştır.

---

## Kullanılan Bulut Teknolojileri

Bu çalışmada aşağıdaki teknolojiler ve servisler kullanılmıştır:

- Amazon Web Services (AWS)
- Amazon EC2 (Elastic Compute Cloud)
- Amazon Linux 2023
- Apache HTTP Server
- SSH (Secure Shell)
- SCP (Secure Copy Protocol)

---

## Uygulamanın Bulut Ortamına Dağıtımı

Portfolio web sitesi, AWS üzerinde oluşturulan bir EC2 instance’ı üzerinde çalıştırılmıştır. Instance oluşturma sürecinde uygun AMI ve instance türü seçilmiş, güvenli erişim için anahtar çifti (key pair) oluşturulmuş ve gerekli ağ izinleri Security Groups aracılığıyla tanımlanmıştır.

Sunucuya SSH protokolü kullanılarak uzaktan bağlantı sağlanmış, sistem güncellemeleri yapılmış ve Apache HTTP Server kurulmuştur. Ardından, web sitesine ait dosyalar SCP kullanılarak sunucuya aktarılmış ve Apache’nin varsayılan web dizinine yerleştirilmiştir. Dosya sahipliği ve erişim izinleri düzenlenerek web sunucusunun dosyalara sorunsuz erişimi sağlanmıştır.

---

## Repository İçeriği

Bu repository içerisinde, proje kapsamında hazırlanan rapor dosyası ve portfolio web sitesine ait statik dosyalar yer almaktadır. Repository, projenin teknik sürecini belgelemek ve çalışmanın tekrar edilebilirliğini sağlamak amacıyla düzenlenmiştir.

---

## Hazırlayan

**Dilara Top**  
B221200573
Sakarya Üniversitesi  
Bilişim Sistemleri Mühendisliği  
Bulut Bilişim Dersi  
