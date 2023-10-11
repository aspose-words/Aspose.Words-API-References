---
title: DigitalSignatureUtil.LoadSignatures
second_title: Aspose.Words for .NET API Referansı
description: DigitalSignatureUtil yöntem. Belgeden dijital imzaları yükler.
type: docs
weight: 10
url: /tr/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(string) {#loadsignatures_1}

Belgeden dijital imzaları yükler.

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Belgenin yolu. |

### Geri dönüş değeri

Dijital imzaların toplanması. Dosya imzalanmamışsa boş koleksiyonu döndürür.

### Örnekler

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

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* toplantı [Aspose.Words](../../../)

---

## LoadSignatures(Stream) {#loadsignatures}

Belgeden dijital imzaları akışı kullanarak yükler.

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Belgeyle akış gerçekleştirin. |

### Geri dönüş değeri

Dijital imzaların toplanması. Dosya imzalanmamışsa boş koleksiyonu döndürür.

### Örnekler

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

### Ayrıca bakınız

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* toplantı [Aspose.Words](../../../)


