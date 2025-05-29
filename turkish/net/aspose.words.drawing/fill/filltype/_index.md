---
title: Fill.FillType
linktitle: FillType
articleTitle: FillType
second_title: .NET için Aspose.Words
description: FillType özelliğini etkili bir şekilde nasıl ayarlayacağınızı ve daha iyi görsel etki için özelleştirilebilir dolgu seçenekleriyle tasarımınızı nasıl geliştireceğinizi keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.drawing/fill/filltype/
---
## Fill.FillType property

Bir dolgu türü alır.

```csharp
public FillType FillType { get; }
```

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

* enum [FillType](../../filltype/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
