---
title: Paragraph.IsEndOfHeaderFooter
linktitle: IsEndOfHeaderFooter
articleTitle: IsEndOfHeaderFooter
second_title: .NET için Aspose.Words
description: Paragraflar için IsEndOfHeaderFooter özelliğini keşfedin. Bir paragrafın HeaderFooter'daki son paragraf olup olmadığını kolayca belirleyerek belge yapısını geliştirin.
type: docs
weight: 70
url: /tr/net/aspose.words/paragraph/isendofheaderfooter/
---
## Paragraph.IsEndOfHeaderFooter property

Bu paragraf, paragrafın son paragrafıysa doğrudur.[`HeaderFooter`](../../headerfooter/) (ana metin hikayesi)[`Section`](../../section/) ; aksi takdirde yanlış.

```csharp
public bool IsEndOfHeaderFooter { get; }
```

## Örnekler

Üstbilgi ve altbilginin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Bir başlık oluşturun ve ona bir paragraf ekleyin. Bu paragraftaki metin
// bu bölümün her sayfasının en üstünde, ana gövde metninin üstünde görünecektir.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Bir altbilgi oluşturun ve ona bir paragraf ekleyin. Bu paragraftaki metin
// Bu bölümün her sayfasının en altında, ana gövde metninin altında görünecektir.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Ayrıca bakınız

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
