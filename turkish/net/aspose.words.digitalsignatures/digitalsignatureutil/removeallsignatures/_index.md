---
title: DigitalSignatureUtil.RemoveAllSignatures
second_title: Aspose.Words for .NET API Referansı
description: DigitalSignatureUtil yöntem. Tüm dijital imzaları kaynak dosyadan kaldırır ve imzasız dosyayı hedef dosyaya yazar.
type: docs
weight: 20
url: /tr/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(string, string) {#removeallsignatures_1}

Tüm dijital imzaları kaynak dosyadan kaldırır ve imzasız dosyayı hedef dosyaya yazar.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

### Örnekler

Dijital olarak imzalanmış bir belgeden dijital imzaların nasıl kaldırılacağını gösterir.

```csharp
// Dijital imzaları kaldırmak için DigitalSignatureUtil sınıfını kullanmanın iki yolu vardır.
// imzasız bir kopyasını yerel dosya sisteminde başka bir yere kaydederek imzalı bir belgeden.
// 1 - Dosya adı dizelerine göre hem imzalı belgenin hem de imzasız kopyanın konumlarını belirleyin:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Dosya akışlarına göre hem imzalı belgenin hem de imzasız kopyanın konumlarını belirleyin:
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

* class [DigitalSignatureUtil](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* toplantı [Aspose.Words](../../../)

---

## RemoveAllSignatures(Stream, Stream) {#removeallsignatures}

Kaynak akıştaki belgedeki tüm dijital imzaları kaldırır ve imzasız belgeyi hedef akışa yazar.

**Çıktı akışın başına yazılacak ve akış boyutu içerik uzunluğu ile güncellenecektir.**

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

### Örnekler

Dijital olarak imzalanmış bir belgeden dijital imzaların nasıl kaldırılacağını gösterir.

```csharp
// Dijital imzaları kaldırmak için DigitalSignatureUtil sınıfını kullanmanın iki yolu vardır.
// imzasız bir kopyasını yerel dosya sisteminde başka bir yere kaydederek imzalı bir belgeden.
// 1 - Dosya adı dizelerine göre hem imzalı belgenin hem de imzasız kopyanın konumlarını belirleyin:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Dosya akışlarına göre hem imzalı belgenin hem de imzasız kopyanın konumlarını belirleyin:
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

* class [DigitalSignatureUtil](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* toplantı [Aspose.Words](../../../)


