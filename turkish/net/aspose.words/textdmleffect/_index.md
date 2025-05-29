---
title: TextDmlEffect Enum
linktitle: TextDmlEffect
articleTitle: TextDmlEffect
second_title: .NET için Aspose.Words
description: Dinamik DML efektleriyle metin çalıştırmalarını geliştirmek için Aspose.Words.TextDmlEffect enum'unu keşfedin. Belge sunumunuzu zahmetsizce yükseltin!
type: docs
weight: 7260
url: /tr/net/aspose.words/textdmleffect/
---
## TextDmlEffect enumeration

Metin çalışmaları için Dml metin efekti.

```csharp
public enum TextDmlEffect
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Glow | `0` | Nesnenin kenarlarının dışına renkli bulanık bir anahat eklenerek oluşturulan parlama efekti. |
| Fill | `1` | Kaplama efektini doldur. |
| Shadow | `2` | Gölge efekti. |
| Outline | `3` | Anahat efekti. |
| Effect3D | `4` | 3D efekti. |
| Reflection | `5` | Yansıma efekti. |

## Örnekler

Bir çalışmanın DrawingML metin efekti gösterip göstermediğinin nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "DrawingML text effects.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.True(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection));
Assert.True(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D));
Assert.True(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill));
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
