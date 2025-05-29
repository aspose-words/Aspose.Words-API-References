---
title: DigitalSignatureUtil.RemoveAllSignatures
linktitle: RemoveAllSignatures
articleTitle: RemoveAllSignatures
second_title: .NET için Aspose.Words
description: DigitalSignatureUtil'in RemoveAllSignatures metoduyla tüm dijital imzaları zahmetsizce kaldırın. İmzalı dosyalarınızı kolayca temiz, imzasız versiyonlara dönüştürün!
type: docs
weight: 20
url: /tr/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(*string, string*) {#removeallsignatures_1}

Kaynak dosyadan tüm dijital imzaları kaldırır ve imzasız dosyayı hedef dosyaya yazar.

Dijital imza kaldırma için aşağıdaki formatlar uyumludur: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

## Örnekler

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

* class [DigitalSignatureUtil](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)

---

## RemoveAllSignatures(*Stream, Stream*) {#removeallsignatures}

Kaynak akışındaki belgeden tüm dijital imzaları kaldırır ve imzasız belgeyi hedef akışına yazar.

**Çıktı, akışın başlangıcına yazılacak ve akış boyutu içerik uzunluğuna göre güncellenecektir.**

Dijital imza kaldırma için aşağıdaki formatlar uyumludur: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

## Örnekler

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

* class [DigitalSignatureUtil](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
