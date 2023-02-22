---
title: Enum DigitalSignatureType
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.DigitalSignatures.DigitalSignatureType Sıralama. Dijital imzanın türünü belirtir.
type: docs
weight: 390
url: /tr/net/aspose.words.digitalsignatures/digitalsignaturetype/
---
## DigitalSignatureType enumeration

Dijital imzanın türünü belirtir.

```csharp
public enum DigitalSignatureType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Unknown | `0` | Bir hatayı, bilinmeyen dijital imza türünü gösterir. |
| CryptoApi | `1` | Microsoft Word 97-2003 .DOC ikili belgelerinde kullanılan Crypto API imza yöntemi. |
| XmlDsig | `2` | OOXML ve OpenDocument belgelerinde kullanılan XmlDsig imza yöntemi. |

### Örnekler

X.509 sertifikalarıyla belgelerin nasıl imzalanacağını gösterir.

```csharp
// Bir belgenin imzalanmadığını doğrulayın.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Belgeyi imzalamak için kullanacağımız bir PKCS12 dosyasından bir CertificateHolder nesnesi oluşturun.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Belgenin imzalı bir kopyasını yerel dosya sistemine kaydetmenin iki yolu vardır:
// 1 - Bir belgeyi yerel sistem dosya adıyla atayın ve imzalı bir kopyayı başka bir dosya adıyla belirtilen bir konuma kaydedin.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

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

* ad alanı [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../)


