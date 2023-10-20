---
title: SignOptions.SignTime
linktitle: SignTime
articleTitle: SignTime
second_title: Aspose.Words for .NET
description: SignOptions SignTime mülk. İmzalama tarihi. Varsayılan değerşimdiki zaman Now C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words.digitalsignatures/signoptions/signtime/
---
## SignOptions.SignTime property

İmzalama tarihi. Varsayılan değer:**şimdiki zaman** (Now).

```csharp
public DateTime SignTime { get; set; }
```

## Örnekler

Belgelerin dijital olarak nasıl imzalanacağını gösterir.

```csharp
// PKCS#12 deposundan özel anahtar içermesi gereken bir X.509 sertifikası oluşturun.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Yeni dijital imzamızla uygulanacak bir yorum ve tarih oluşturun.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// İmzasız bir belgeyi dosya akışı aracılığıyla yerel dosya sisteminden alın,
// ardından çıktı dosyası akışının dosya adına göre belirlenen imzalı bir kopyasını oluşturun.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Ayrıca bakınız

* class [SignOptions](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
