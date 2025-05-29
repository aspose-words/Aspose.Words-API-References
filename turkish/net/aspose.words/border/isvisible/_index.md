---
title: Border.IsVisible
linktitle: IsVisible
articleTitle: IsVisible
second_title: .NET için Aspose.Words
description: Border IsVisible özelliğinin, LineStyle uygulandığında true döndürerek tasarımınızı nasıl geliştirdiğini keşfedin. Bu önemli özellik ile kullanıcı arayüzünüzü optimize edin!
type: docs
weight: 30
url: /tr/net/aspose.words/border/isvisible/
---
## Border.IsVisible property

Geri Döndürür`doğru` eğer[`LineStyle`](../linestyle/) değilNone .

```csharp
public bool IsVisible { get; }
```

## Örnekler

Bir paragraftan kenarlıkların nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Her paragrafın kendine ait bir kenarlık kümesi vardır.
// Bu kenarlıkların görünümüne ilişkin ayarlara paragraf format nesnesi aracılığıyla erişebiliriz.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

 // ClearFormatting metodunu çalıştırarak bir kenarlığı tek seferde kaldırabiliriz.
// Bu metodu bir paragrafın her kenarlığında çalıştırmak, tüm kenarlıklarını kaldıracaktır.
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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
