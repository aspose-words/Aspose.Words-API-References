---
title: DigitalSignatureUtil.LoadSignatures
linktitle: LoadSignatures
articleTitle: LoadSignatures
second_title: .NET için Aspose.Words
description: DigitalSignatureUtil LoadSignatures yöntemiyle belgelerinizden dijital imzaları zahmetsizce yükleyin. İş akışınızı bugün geliştirin!
type: docs
weight: 10
url: /tr/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(*string*) {#loadsignatures_1}

Belgeden dijital imzaları yükler.

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Belgeye giden yol. |

### Geri dönüş değeri

Dijital imzaların koleksiyonu. Dosya imzalanmamışsa boş koleksiyon döndürür.

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

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)

---

## LoadSignatures(*Stream*) {#loadsignatures}

Akışı kullanarak belgeden dijital imzaları yükler.

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Belgeyle birlikte yayınlayın. |

### Geri dönüş değeri

Dijital imzaların koleksiyonu. Dosya imzalanmamışsa boş koleksiyon döndürür.

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

### Ayrıca bakınız

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
