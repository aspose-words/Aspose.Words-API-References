---
title: Fill.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: .NET için Aspose.Words
description: Tasarımlarınızda özelleştirilebilir görsel efektler için dolgu şeffaflığını 0,0 (opak) ile 1,0 (şeffaf) arasında ayarlayın. Projenizin estetiğini bugün geliştirin!
type: docs
weight: 200
url: /tr/net/aspose.words.drawing/fill/transparency/
---
## Fill.Transparency property

Belirtilen dolgunun şeffaflık derecesini 0,0 (opak) ile 1,0 (temiz) arasında bir değer olarak alır veya ayarlar.

```csharp
public double Transparency { get; set; }
```

## Notlar

Bu özellik, özelliğin tam tersidir[`Opacity`](../opacity/).

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
