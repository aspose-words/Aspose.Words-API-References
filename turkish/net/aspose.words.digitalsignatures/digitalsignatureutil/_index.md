---
title: DigitalSignatureUtil Class
linktitle: DigitalSignatureUtil
articleTitle: DigitalSignatureUtil
second_title: .NET için Aspose.Words
description: Belgeleri güvenli dijital imzalarla kolayca imzalamak için Aspose.Words.DigitalSignatures.DigitalSignatureUtil sınıfını keşfedin. Belge bütünlüğünü bugün geliştirin!
type: docs
weight: 610
url: /tr/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

Belgeyi imzalamak için yöntemler sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Dijital İmzalarla Çalışın](https://docs.aspose.com/words/net/working-with-digital-signatures/) belgeleme makalesi.

```csharp
public static class DigitalSignatureUtil
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures)(*Stream*) | Akışı kullanarak belgeden dijital imzaları yükler. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures_1)(*string*) | Belgeden dijital imzaları yükler. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures)(*Stream, Stream*) | Kaynak akışındaki belgeden tüm dijital imzaları kaldırır ve imzasız belgeyi hedef akışına yazar. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures_1)(*string, string*) | Kaynak dosyadan tüm dijital imzaları kaldırır ve imzasız dosyayı hedef dosyaya yazar. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign)(*Stream, Stream, [CertificateHolder](../certificateholder/)*) | Verileni kullanarak kaynak belgeyi işaretler[`CertificateHolder`](../certificateholder/) dijital imza ile imzalanmış belgeyi hedef akışa yazar. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_2)(*string, string, [CertificateHolder](../certificateholder/)*) | Verileni kullanarak kaynak belgeyi işaretler[`CertificateHolder`](../certificateholder/) dijital imza ile imzalanmış belgeyi hedef dosyaya yazar. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_1)(*Stream, Stream, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Verileni kullanarak kaynak belgeyi işaretler[`CertificateHolder`](../certificateholder/) Ve[`SignOptions`](../signoptions/) dijital imza ile imzalanmış belgeyi hedef akışa yazar. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_3)(*string, string, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Verileni kullanarak kaynak belgeyi işaretler[`CertificateHolder`](../certificateholder/) Ve[`SignOptions`](../signoptions/) dijital imza ile imzalanmış belgeyi hedef dosyaya yazar. |

## Notlar

Dijital imza, Belge Nesne Modeli yerine dosya içeriğiyle çalıştığı için bu yöntemler ayrı bir sınıfa konur.

Desteklenen biçimler şunlardır: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

## Örnekler

Dijital olarak imzalanmış bir belgeden imzaların nasıl yükleneceğini gösterir.

```csharp
// DigitalSignatureUtil sınıfını kullanarak imzalanmış bir belgenin dijital imza koleksiyonunu yüklemenin iki yolu vardır.
// 1 - Yerel dosya sisteminden bir belgeden yükleme dosya adı:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Eğer bu koleksiyon boş değilse, belgenin dijital olarak imzalandığını doğrulayabiliriz.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Bir FileStream'den bir belgeden yükleme:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

Dijital olarak imzalanmış bir belgeden dijital imzaların nasıl kaldırılacağını gösterir.

```csharp
// Dijital imzaları kaldırmak için DigitalSignatureUtil sınıfını kullanmanın iki yolu vardır
// imzalanmış bir belgenin imzasız bir kopyasını yerel dosya sisteminin başka bir yerine kaydederek.
// 1 - Dosya adı dizelerine göre hem imzalı belgenin hem de imzasız kopyanın yerlerini belirle:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Dosya akışları ile hem imzalı belgenin hem de imzasız kopyanın yerlerini belirle:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Her iki çıktı belgemizin de dijital imzaya sahip olmadığını doğrulayın.
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").Count);
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").Count);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../)
