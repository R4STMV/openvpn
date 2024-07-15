# OpenVPN Quraşdırıcısı

Müxtəlif Linux distribusiyalarında cəmi bir neçə dəqiqə ərzində öz təhlükəsiz OpenVPN serverinizi qurun.

## Xüsusiyyətlər

- OpenVPN serverinin asan quraşdırılması və idarə edilməsi
- Debian, Ubuntu, Fedora, CentOS, Arch Linux, Oracle Linux, Rocky Linux və AlmaLinux dəstəyi
- Fərdiləşdirilə bilən şifrələmə parametrləri
- IPv6 dəstəyi
- Müxtəlif DNS həlledici seçimləri
- TCP və UDP protokol dəstəyi
- Sıxışdırma seçimləri (təhlükəsizlik üçün standart olaraq deaktivdir)
- İmtiyazsız rejim
- Windows 10 DNS sızma qoruması
- Müştərilər üçün istəyə bağlı parol qoruması

## Sürətli Başlanğıc

1. Skripti yükləyin:
   ```bash
   curl -O https://raw.githubusercontent.com/R4STMV/openvpn-install/master/openvpn-install.sh
   chmod +x openvpn-install.sh
   ```

2. Skripti işə salın:
   ```bash
   ./openvpn-install.sh
   ```

3. VPN serverinizi qurmaq üçün təlimatları izləyin.

4. Quraşdırmadan sonra müştəri konfiqurasiya fayllarını (`.ovpn`) ev qovluğunuzda tapacaqsınız.

## İstifadə

Skripti yenidən işə salaraq:
- Müştəri əlavə edin
- Müştərini silin
- OpenVPN-i silin

## Başsız Quraşdırma

Avtomatlaşdırılmış quraşdırma üçün istifadə edin:

```bash
AUTO_INSTALL=y ./openvpn-install.sh
```

Dəyişənləri lazım olduğu kimi fərdiləşdirin:

```bash
APPROVE_INSTALL=y
APPROVE_IP=y
IPV6_SUPPORT=n
PORT_CHOICE=1
PROTOCOL_CHOICE=1
DNS=1
COMPRESSION_ENABLED=n
CUSTOMIZE_ENC=n
CLIENT=clientname
PASS=1
```

## Uyğunluq

| Distribusiya | Dəstək |
|--------------|--------|
| AlmaLinux 8 | ✅ |
| Amazon Linux 2 | ✅ |
| Arch Linux | ✅ |
| CentOS 7 | ✅ 🤖 |
| CentOS Stream >= 8 | ✅ 🤖 |
| Debian >= 10 | ✅ 🤖 |
| Fedora >= 35 | ✅ 🤖 |
| Oracle Linux 8 | ✅ |
| Rocky Linux 8 | ✅ |
| Ubuntu >= 18.04 | ✅ 🤖 |

🤖 = Müntəzəm olaraq test edilir

## Qeydlər

- amd64 arxitekturasında test edilmişdir
- Daha köhnə versiyalarda işləyə bilər, lakin rəsmi olaraq dəstəklənmir
- systemd tələb edir
