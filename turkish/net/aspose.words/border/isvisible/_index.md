---
title: Border.IsVisible
second_title: Aspose.Words for .NET API Referansı
description: Border mülk. İadelerdoğru EğerLineStyle değilNone .
type: docs
weight: 30
url: /tr/net/aspose.words/border/isvisible/
---
## Border.IsVisible property

İadeler`doğru` Eğer[`LineStyle`](../linestyle/) değilNone .

```csharp
public bool IsVisible { get; }
```

### Örnekler

Paragraftaki kenarlıkların nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Her paragrafın ayrı bir kenarlıkları vardır.
// Bu kenarlıkların görünümüne ilişkin ayarlara paragraf format nesnesi üzerinden erişebiliriz.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

 // ClearFormatting metodunu çalıştırarak kenarlığı tek seferde kaldırabiliriz.
// Bu yöntemi bir paragrafın her kenarlığında çalıştırmak, paragrafın tüm kenarlıklarını kaldıracaktır.
foreach (Border border in borders)
    border.ClearFormatting();

Assert.AreEqual(Color.Empty.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(0.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.None, borders[0].LineStyle);
Assert.IsFalse(borders[0].IsVisible);

doc.Save(ArtifactsDir + "Border.ClearFormatting.docx");
```

### Ayrıca bakınız

* class [Border](../)
* ad alanı [Aspose.Words](../../border/)
* toplantı [Aspose.Words](../../../)


