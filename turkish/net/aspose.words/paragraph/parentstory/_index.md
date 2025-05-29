---
title: Paragraph.ParentStory
linktitle: ParentStory
articleTitle: ParentStory
second_title: .NET için Aspose.Words
description: Belgenizin yapısını Gövde veya Üstbilgi ve Altbilgi seçenekleriyle geliştirerek, üst bölüm düzeyindeki hikayelere kolayca erişmek için Paragraf ÜstHikaye özelliğini keşfedin.
type: docs
weight: 210
url: /tr/net/aspose.words/paragraph/parentstory/
---
## Paragraph.ParentStory property

Ana bölüm düzeyindeki hikayeyi alır.[`Body`](../../body/) veya[`HeaderFooter`](../../headerfooter/) .

```csharp
public Story ParentStory { get; }
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

* class [Story](../../story/)
* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
