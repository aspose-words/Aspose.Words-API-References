---
title: ParagraphFormat.PageBreakBefore
linktitle: PageBreakBefore
articleTitle: PageBreakBefore
second_title: .NET için Aspose.Words
description: ParagraphFormat PageBreakBefore özelliğini keşfedin, gelişmiş belge biçimlendirmesi ve okunabilirliği için paragraflardan önceki sayfa sonlarını kolayca kontrol edin.
type: docs
weight: 270
url: /tr/net/aspose.words/paragraphformat/pagebreakbefore/
---
## ParagraphFormat.PageBreakBefore property

Paragraftan önce bir sayfa sonu zorlanırsa doğrudur.

```csharp
public bool PageBreakBefore { get; set; }
```

## Örnekler

Sayfa sonlarının başında olduğu paragrafların nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Her paragrafın başına bir sayfa sonu uygulamak için bu bayrağı "doğru" olarak ayarlayın
// belge oluşturucunun bu ParagraphFormat yapılandırması altında oluşturacağı.
// İlk paragrafa sayfa sonu eklenmeyecektir.
// Her yeni paragrafı aynı sayfada başlatmak için bu bayrağı "yanlış" olarak bırakın
// önceki gibi, yeterli alan varsa.
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
