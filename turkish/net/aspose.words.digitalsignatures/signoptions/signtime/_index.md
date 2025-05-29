---
title: SignOptions.SignTime
linktitle: SignTime
articleTitle: SignTime
second_title: .NET için Aspose.Words
description: Zahmetsiz imzalama için SignOptions SignTime'ı keşfedin. İmzalama tarihini varsayılan olarak geçerli saate kolayca ayarlayın. Belge sürecinizi kolaylaştırın!
type: docs
weight: 70
url: /tr/net/aspose.words.digitalsignatures/signoptions/signtime/
---
## SignOptions.SignTime property

İmzalama tarihi. Varsayılan değer**şimdiki zaman** (Now)

```csharp
public DateTime SignTime { get; set; }
```

## Örnekler

Belgelerin dijital olarak nasıl imzalanacağını gösterir.

```csharp
// Özel bir anahtar içermesi gereken bir PKCS#12 deposundan bir X.509 sertifikası oluşturun.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Yeni dijital imzamızla uygulanacak bir yorum ve tarih oluşturun.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Yerel dosya sisteminden bir dosya akışı aracılığıyla imzalanmamış bir belge alın,
// daha sonra çıktı dosya akışının dosya adına göre belirlenen imzalı bir kopyasını oluşturur.
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
