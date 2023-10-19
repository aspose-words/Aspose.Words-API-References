---
title: DigitalSignatureUtil.RemoveAllSignatures
linktitle: RemoveAllSignatures
articleTitle: RemoveAllSignatures
second_title: Aspose.Words for .NET
description: DigitalSignatureUtil RemoveAllSignatures yöntem. Kaynak dosyadaki tüm dijital imzaları kaldırır ve imzasız dosyayı hedef dosyaya yazar C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(*string, string*) {#removeallsignatures_1}

Kaynak dosyadaki tüm dijital imzaları kaldırır ve imzasız dosyayı hedef dosyaya yazar.

Aşağıdaki formatlar dijital imza kaldırma için uyumludur: Doc , Dot , Docx , Dotx , Docm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

## Örnekler

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

* class [DigitalSignatureUtil](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)

---

## RemoveAllSignatures(*Stream, Stream*) {#removeallsignatures}

Kaynak akışındaki belgedeki tüm dijital imzaları kaldırır ve imzasız belgeyi hedef akışa yazar.

**Çıktı akışın başlangıcına yazılacak ve akış boyutu içerik uzunluğuyla güncellenecektir.**

Aşağıdaki formatlar dijital imza kaldırma için uyumludur: Doc , Dot , Docx , Dotx , Docm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

## Örnekler

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

* class [DigitalSignatureUtil](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
