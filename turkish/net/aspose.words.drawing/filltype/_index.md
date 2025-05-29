---
title: FillType Enum
linktitle: FillType
articleTitle: FillType
second_title: .NET için Aspose.Words
description: Gelişmiş belge tasarımı için doldurulabilir nesnelerinizi çok yönlü dolgu türleriyle geliştirmek üzere Aspose.Words.Drawing.FillType enum'unu keşfedin.
type: docs
weight: 1280
url: /tr/net/aspose.words.drawing/filltype/
---
## FillType enumeration

Doldurulabilir bir nesne için dolgu türünü belirtir.

```csharp
public enum FillType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Solid | `1` | Katı dolgu. |
| Patterned | `2` | Desenli dolgu. |
| Gradient | `3` | Degrade dolgusu. |
| Textured | `4` | Dokulu dolgu. |
| Background | `5` | Dolgu arka planla aynıdır. |
| Picture | `6` | Resim dolgusu. |

## Örnekler

Herhangi bir dolgunun nasıl tekrar katı dolguya dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// İlk Çalıştırmanın Fontu için Fill nesnesini al.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Fontun Fill özelliklerini kontrol et.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Dolgu tipini düz yeşil renkte olacak şekilde değiştiriyoruz.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
