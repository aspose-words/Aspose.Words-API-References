---
title: Fill.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words for .NET
description: Fill Color mülk. Dolgunun ön plan rengini temsil eden bir Color nesnesini alır veya ayarlar C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing/fill/color/
---
## Fill.Color property

Dolgunun ön plan rengini temsil eden bir Color nesnesini alır veya ayarlar.

```csharp
public Color Color { get; set; }
```

## Notlar

Bu özellik alfa bileşenini korur.Color , aksine[`ForeColor`](../forecolor/)tamamen opak renge sıfırlayan özellik.

## Örnekler

Herhangi bir dolgunun tekrar katı dolguya nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// İlk Çalıştırmanın Yazı Tipi için Dolgu nesnesini alın.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Yazı Tipinin Dolgu özelliklerini kontrol edin.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Dolgunun türünü tek tip yeşil renkte Katı olarak değiştirin.
fill.Solid(Color.Green);
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Ayrıca bakınız

* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
