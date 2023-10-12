---
title: LoadOptions.Password
second_title: Aspose.Words for .NET API Referansı
description: LoadOptions mülk. Şifrelenmiş bir belgeyi açmak için parolayı alır veya ayarlar. Olabilirhükümsüz veya boş dize. Varsayılanhükümsüz .
type: docs
weight: 110
url: /tr/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

Şifrelenmiş bir belgeyi açmak için parolayı alır veya ayarlar. Olabilir`hükümsüz` veya boş dize. Varsayılan:`hükümsüz` .

```csharp
public string Password { get; set; }
```

### Notlar

Şifrelenmiş bir belgeyi açmak için şifreyi bilmeniz gerekir. Belge şifrelenmemişse bunu şu şekilde ayarlayın:`hükümsüz` veya boş dize.

### Örnekler

Şifrelenmiş belge dosyasının nasıl imzalanacağını gösterir.

```csharp
// PKCS#12 deposundan özel anahtar içermesi gereken bir X.509 sertifikası oluşturun.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Yeni dijital imzamızla uygulanacak bir yorum, tarih ve şifre çözme şifresi oluşturun.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// İmzasız giriş belgesi için yerel bir sistem dosya adı ve dijital olarak imzalanmış yeni kopyası için bir çıktı dosya adı belirleyin.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)


