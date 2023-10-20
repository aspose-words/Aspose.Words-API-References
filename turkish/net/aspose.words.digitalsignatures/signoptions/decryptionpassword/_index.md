---
title: SignOptions.DecryptionPassword
linktitle: DecryptionPassword
articleTitle: DecryptionPassword
second_title: Aspose.Words for .NET
description: SignOptions DecryptionPassword mülk. Kaynak belgenin şifresini çözmek için kullanılan parola. Varsayılan değerboş dize Empty C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.digitalsignatures/signoptions/decryptionpassword/
---
## SignOptions.DecryptionPassword property

Kaynak belgenin şifresini çözmek için kullanılan parola. Varsayılan değer:**boş dize** (Empty).

```csharp
public string DecryptionPassword { get; set; }
```

## Notlar

OOXML belgesi şifrelenmişse, imzalanmadan önce kaynak belgenin şifresini çözmek için şifre çözme parolasını sağlamalısınız. Bu, ikili DOC biçimindeki belgeler için gerekli değildir.

## Örnekler

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

* class [SignOptions](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
