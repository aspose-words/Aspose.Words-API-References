---
title: LoadOptions.Password
linktitle: Password
articleTitle: Password
second_title: .NET için Aspose.Words
description: Şifrelenmiş belgelerinizi LoadOptions Password özelliğiyle zahmetsizce yönetin. Sorunsuz erişim için parolanızı güvenli bir şekilde ayarlayın veya geri alın.
type: docs
weight: 110
url: /tr/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

Şifrelenmiş bir belgeyi açmak için parolayı alır veya ayarlar. Şu şekilde olabilir:`hükümsüz` veya boş dize. Varsayılan`hükümsüz` .

```csharp
public string Password { get; set; }
```

## Notlar

Şifrelenmiş bir belgeyi açmak için parolayı bilmeniz gerekir. Belge şifrelenmemişse, bunu şu şekilde ayarlayın:`hükümsüz` veya boş dize.

## Örnekler

Şifrelenmiş belge dosyasının nasıl imzalanacağını gösterir.

```csharp
// Özel bir anahtar içermesi gereken bir PKCS#12 deposundan bir X.509 sertifikası oluşturun.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Yeni dijital imzamızla uygulanacak bir yorum, tarih ve şifre çözme şifresi oluşturun.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// İmzalanmamış girdi belgesi için yerel bir sistem dosya adı ve yeni dijital olarak imzalanmış kopyası için bir çıktı dosya adı ayarlayın.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
