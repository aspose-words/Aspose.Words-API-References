---
title: DigitalSignatureUtil Class
linktitle: DigitalSignatureUtil
articleTitle: DigitalSignatureUtil
second_title: Aspose.Words for .NET
description: Aspose.Words.DigitalSignatures.DigitalSignatureUtil sınıf. Belgeyi imzalamak için yöntemler sağlar C#'da.
type: docs
weight: 410
url: /tr/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

Belgeyi imzalamak için yöntemler sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Dijital İmzalarla Çalışma](https://docs.aspose.com/words/net/working-with-digital-signatures/) dokümantasyon makalesi.

```csharp
public static class DigitalSignatureUtil
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures)(*Stream*) | Belgeden dijital imzaları akışı kullanarak yükler. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures_1)(*string*) | Belgeden dijital imzaları yükler. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures)(*Stream, Stream*) | Kaynak akışındaki belgedeki tüm dijital imzaları kaldırır ve imzasız belgeyi hedef akışa yazar. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures_1)(*string, string*) | Kaynak dosyadaki tüm dijital imzaları kaldırır ve imzasız dosyayı hedef dosyaya yazar. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign)(*Stream, Stream, [CertificateHolder](../certificateholder/)*) | Verilenleri kullanarak kaynak belgeyi imzalar[`CertificateHolder`](../certificateholder/)dijital imza ile imzalanır ve imzalı belgeyi hedef akışa yazar. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_2)(*string, string, [CertificateHolder](../certificateholder/)*) | Verilenleri kullanarak kaynak belgeyi imzalar[`CertificateHolder`](../certificateholder/) dijital imza ile imzalanır ve imzalı belgeyi hedef dosyaya yazar. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_1)(*Stream, Stream, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Verilenleri kullanarak kaynak belgeyi imzalar[`CertificateHolder`](../certificateholder/) Ve[`SignOptions`](../signoptions/) dijital imzalı ve imzalı belgeyi hedef akışa yazar. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_3)(*string, string, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Verilenleri kullanarak kaynak belgeyi imzalar[`CertificateHolder`](../certificateholder/) Ve[`SignOptions`](../signoptions/) dijital imzayla imzalanır ve imzalı belgeyi hedef dosyaya yazar. |

## Notlar

Dijital imza, Belge Nesne Modeli yerine dosya içeriğiyle çalıştığı için bu yöntemler ayrı bir sınıfa konur.

Desteklenen formatlarDoc VeDocx.

## Örnekler

Dijital olarak imzalanmış bir belgeden imzaların nasıl yükleneceğini gösterir.

```csharp
// İmzalı bir belgenin dijital imza koleksiyonunu DigitalSignatureUtil sınıfını kullanarak yüklemenin iki yolu vardır.
// 1 - Yerel dosya sistemi dosya adından bir belgeden yükleyin:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Bu koleksiyon boş değilse belgenin dijital olarak imzalandığını doğrulayabiliriz.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - FileStream'den bir belgeden yükleyin:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

Dijital imzalı bir belgeden dijital imzaların nasıl kaldırılacağını gösterir.

```csharp
// Dijital imzaları kaldırmak için DigitalSignatureUtil sınıfını kullanmanın iki yolu vardır
// imzalı bir belgenin imzasız bir kopyasını yerel dosya sisteminde başka bir yere kaydederek.
// 1 - Hem imzalı belgenin hem de imzasız kopyanın konumlarını dosya adı dizelerine göre belirleyin:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Hem imzalı belgenin hem de imzasız kopyanın konumlarını dosya akışlarına göre belirleyin:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Her iki çıktı belgemizin de dijital imzası olmadığını doğrulayın.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../)
