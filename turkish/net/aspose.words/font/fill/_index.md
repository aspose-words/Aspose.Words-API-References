---
title: Font.Fill
linktitle: Fill
articleTitle: Fill
second_title: .NET için Aspose.Words
description: Metninizin görünümünü özelleştirilebilir dolgu biçimlendirmesiyle geliştirerek cilalı, profesyonel bir görünüm elde etmek için Font Dolgusu özelliğini keşfedin.
type: docs
weight: 130
url: /tr/net/aspose.words/font/fill/
---
## Font.Fill property

için doldurma biçimlendirmesini alır[`Font`](../) .

```csharp
public Fill Fill { get; }
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

* class [Fill](../../../aspose.words.drawing/fill/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
