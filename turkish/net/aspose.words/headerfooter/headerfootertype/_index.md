---
title: HeaderFooter.HeaderFooterType
linktitle: HeaderFooterType
articleTitle: HeaderFooterType
second_title: .NET için Aspose.Words
description: Gelişmiş biçimlendirme denetimi için belgenizin üstbilgi ve altbilgi türlerine kolayca erişmek ve bunları yönetmek amacıyla HeaderFooterType özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words/headerfooter/headerfootertype/
---
## HeaderFooter.HeaderFooterType property

Bu başlık/altbilginin türünü alır.

```csharp
public HeaderFooterType HeaderFooterType { get; }
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

* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
