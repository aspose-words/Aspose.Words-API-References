---
title: ParagraphFormat.PageBreakBefore
linktitle: PageBreakBefore
articleTitle: PageBreakBefore
second_title: Aspose.Words for .NET
description: ParagraphFormat PageBreakBefore mülk. Paragraftan önce sayfa sonu zorunluysa doğrudur C#'da.
type: docs
weight: 260
url: /tr/net/aspose.words/paragraphformat/pagebreakbefore/
---
## ParagraphFormat.PageBreakBefore property

Paragraftan önce sayfa sonu zorunluysa doğrudur.

```csharp
public bool PageBreakBefore { get; set; }
```

## Örnekler

Başında sayfa sonları bulunan paragrafların nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Her paragrafın başlangıcına sayfa sonu uygulamak için bu bayrağı "true" olarak ayarlayın
// belge oluşturucunun bu ParagraphFormat yapılandırması altında oluşturacağı.
// İlk paragrafta sayfa sonu verilmeyecektir.
// Her yeni paragrafın aynı sayfada başlaması için bu işareti "yanlış" olarak bırakın
// yeterli alan olması koşuluyla önceki gibi.
builder.ParagraphFormat.PageBreakBefore = pageBreakBefore;

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

LayoutCollector layoutCollector = new LayoutCollector(doc);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

if (pageBreakBefore)
{
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[0]));
    Assert.AreEqual(2, layoutCollector.GetStartPageIndex(paragraphs[1]));
}
else
{
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[0]));
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[1]));
}

doc.Save(ArtifactsDir + "ParagraphFormat.PageBreakBefore.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
