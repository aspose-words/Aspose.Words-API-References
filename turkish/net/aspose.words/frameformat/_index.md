---
title: FrameFormat Class
linktitle: FrameFormat
articleTitle: FrameFormat
second_title: .NET için Aspose.Words
description: Paragraflarda gelişmiş çerçeve biçimlendirmesi için Aspose.Words.FrameFormat sınıfını keşfedin. Belge tasarımınızı kusursuz entegrasyon ve esneklikle geliştirin.
type: docs
weight: 3500
url: /tr/net/aspose.words/frameformat/
---
## FrameFormat class

Bir paragraf için çerçeveyle ilgili biçimlendirmeyi temsil eder.

```csharp
public class FrameFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Height](../../aspose.words/frameformat/height/) { get; } | Belirtilen çerçevenin yüksekliğini alır. |
| [HeightRule](../../aspose.words/frameformat/heightrule/) { get; } | Belirtilen çerçevenin yüksekliğini belirleme kuralını alır. |
| [HorizontalAlignment](../../aspose.words/frameformat/horizontalalignment/) { get; } | Belirtilen çerçevenin yatay hizalamasını alır. |
| [HorizontalDistanceFromText](../../aspose.words/frameformat/horizontaldistancefromtext/) { get; } | Bir çerçeve ile çevresindeki metin arasındaki yatay mesafeyi nokta cinsinden alır. |
| [HorizontalPosition](../../aspose.words/frameformat/horizontalposition/) { get; } | Çerçevenin kenarı ile belirtilen öğe arasındaki yatay mesafeyi alır[`RelativeHorizontalPosition`](./relativehorizontalposition/) mülk. |
| [IsFrame](../../aspose.words/frameformat/isframe/) { get; } | Geri Döndürür`doğru` eğer paragraf bir çerçeve ise. |
| [RelativeHorizontalPosition](../../aspose.words/frameformat/relativehorizontalposition/) { get; } | Bir çerçevenin göreceli yatay konumunu alır. |
| [RelativeVerticalPosition](../../aspose.words/frameformat/relativeverticalposition/) { get; } | Bir çerçevenin göreli dikey konumunu alır. |
| [VerticalAlignment](../../aspose.words/frameformat/verticalalignment/) { get; } | Belirtilen çerçevenin dikey hizalamasını alır. |
| [VerticalDistanceFromText](../../aspose.words/frameformat/verticaldistancefromtext/) { get; } | Bir çerçeve ile çevresindeki metin arasındaki dikey mesafeyi (nokta cinsinden) belirtir. |
| [VerticalPosition](../../aspose.words/frameformat/verticalposition/) { get; } | Çerçevenin kenarı ile belirtilen öğe arasındaki dikey mesafeyi alır[`RelativeVerticalPosition`](./relativeverticalposition/) mülk. |
| [Width](../../aspose.words/frameformat/width/) { get; } | Belirtilen çerçevenin genişliğini noktalar halinde alır. |

## Notlar

Bu nesne her zaman oluşturulur. Bir paragraf bir çerçeveyse, tüm özellikler ilgili değerleri içerecektir, aksi takdirde tüm özellikler varsayılanlarına ayarlanır.

Kullanmak[`IsFrame`](./isframe/)Paragrafın çerçeve olup olmadığını kontrol etmek için.

## Örnekler

Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi edinmenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraph frame.docx");

Paragraph paragraphFrame = doc.FirstSection.Body.Paragraphs.OfType<Paragraph>().First(p => p.FrameFormat.IsFrame);

Assert.AreEqual(233.3d, paragraphFrame.FrameFormat.Width);
Assert.AreEqual(138.8d, paragraphFrame.FrameFormat.Height);
Assert.AreEqual(HeightRule.AtLeast, paragraphFrame.FrameFormat.HeightRule);
Assert.AreEqual(HorizontalAlignment.Default, paragraphFrame.FrameFormat.HorizontalAlignment);
Assert.AreEqual(VerticalAlignment.Default, paragraphFrame.FrameFormat.VerticalAlignment);
Assert.AreEqual(34.05d, paragraphFrame.FrameFormat.HorizontalPosition);
Assert.AreEqual(RelativeHorizontalPosition.Page, paragraphFrame.FrameFormat.RelativeHorizontalPosition);
Assert.AreEqual(9.0d, paragraphFrame.FrameFormat.HorizontalDistanceFromText);
Assert.AreEqual(20.5d, paragraphFrame.FrameFormat.VerticalPosition);
Assert.AreEqual(RelativeVerticalPosition.Paragraph, paragraphFrame.FrameFormat.RelativeVerticalPosition);
Assert.AreEqual(0.0d, paragraphFrame.FrameFormat.VerticalDistanceFromText);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
