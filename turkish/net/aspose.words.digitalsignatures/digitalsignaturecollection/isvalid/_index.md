---
title: DigitalSignatureCollection.IsValid
linktitle: IsValid
articleTitle: IsValid
second_title: .NET için Aspose.Words
description: DigitalSignatureCollection'ın IsValid özelliğiyle belge bütünlüğünü sağlayın. Tüm imzaların geçerli ve bozulmamış olduğunu doğrulayarak güvenliği artırır.
type: docs
weight: 30
url: /tr/net/aspose.words.digitalsignatures/digitalsignaturecollection/isvalid/
---
## DigitalSignatureCollection.IsValid property

Geri Döndürür`doğru`bu koleksiyondaki tüm dijital imzalar geçerliyse ve belgede değişiklik yapılmamışsa Ayrıca şunu da döndürür:`doğru` dijital imzalar yoksa. Geri döner`YANLIŞ` en az bir dijital imza geçersizse.

```csharp
public bool IsValid { get; }
```

## Örnekler

X.509 sertifikalarıyla belgelerin nasıl imzalanacağını gösterir.

```csharp
// Bir belgenin imzalanmadığını doğrulayın.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Belgeyi imzalamak için kullanacağımız PKCS12 dosyasından bir CertificateHolder nesnesi oluşturalım.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Bir belgenin imzalı bir kopyasını yerel dosya sistemine kaydetmenin iki yolu vardır:
// 1 - Bir belgeyi yerel sistem dosya adıyla tanımlayın ve imzalı bir kopyasını başka bir dosya adıyla belirtilen bir konuma kaydedin.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Bir akıştan bir belge alın ve imzalı bir kopyasını başka bir akışa kaydedin.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Lütfen belgenin tüm dijital imzalarının geçerli olduğunu doğrulayın ve ayrıntılarını kontrol edin.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Ayrıca bakınız

* class [DigitalSignatureCollection](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
