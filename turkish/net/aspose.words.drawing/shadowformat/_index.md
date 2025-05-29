---
title: ShadowFormat Class
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: .NET için Aspose.Words
description: Gelişmiş nesne gölge efektleri için Aspose.Words.Drawing.ShadowFormat'ı keşfedin. Özelleştirilebilir gölge biçimlendirme seçenekleriyle belge tasarımınızı yükseltin.
type: docs
weight: 1620
url: /tr/net/aspose.words.drawing/shadowformat/
---
## ShadowFormat class

Bir nesne için gölge biçimlendirmesini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafik Öğelerle Çalışma](https://docs.aspose.com/words/net/working-with-graphic-elements/) belgeleme makalesi.

```csharp
public class ShadowFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Color](../../aspose.words.drawing/shadowformat/color/) { get; } | Bir tane alırColor gölgenin rengini temsil eden nesne. Varsayılan değerBlack . |
| [Type](../../aspose.words.drawing/shadowformat/type/) { get; set; } | Belirtilen değeri alır veya ayarlar[`ShadowType`](../shadowtype/) ShadowFormat. için |
| [Visible](../../aspose.words.drawing/shadowformat/visible/) { get; } | Geri Döndürür`doğru` bu örneğe uygulanan biçimlendirme görünürse. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clear](../../aspose.words.drawing/shadowformat/clear/)() | Gölge biçimini temizler. |

## Örnekler

Gölge renginin nasıl elde edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
