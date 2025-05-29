---
title: Fill.Color
linktitle: Color
articleTitle: Color
second_title: .NET için Aspose.Words
description: Projenizin görsel çekiciliğini artırmak için, tasarımınızın ön plan rengini bir Renk nesnesiyle kolayca özelleştirmek üzere Dolgu Rengi özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing/fill/color/
---
## Fill.Color property

Dolgu için ön plan rengini temsil eden bir Renk nesnesi alır veya ayarlar.

```csharp
public Color Color { get; set; }
```

## Notlar

Bu özellik, alfa bileşenini korurColor , aksine[`ForeColor`](../forecolor/) özelliği, onu tamamen opak renge sıfırlar.

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

* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
