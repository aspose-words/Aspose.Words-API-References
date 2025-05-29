---
title: SignOptions.DecryptionPassword
linktitle: DecryptionPassword
articleTitle: DecryptionPassword
second_title: .NET için Aspose.Words
description: SignOptions'ın DecryptionPassword özelliğiyle belgelerinizin kilidini zahmetsizce açın. Kaynak dosyaları kolayca ve güvenli bir şekilde şifresini çözün; varsayılan boş bir dizedir.
type: docs
weight: 30
url: /tr/net/aspose.words.digitalsignatures/signoptions/decryptionpassword/
---
## SignOptions.DecryptionPassword property

Kaynak belgeyi şifresini çözmek için kullanılan parola. Varsayılan değer**boş dize** (Empty ).

```csharp
public string DecryptionPassword { get; set; }
```

## Notlar

OOXML belgesi şifrelenmişse, imzalanmadan önce kaynak belgenin şifresini çözmek için şifre çözme parolası sağlamalısınız. Bu, ikili DOC biçimindeki belgeler için gerekli değildir.

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

* class [SignOptions](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
