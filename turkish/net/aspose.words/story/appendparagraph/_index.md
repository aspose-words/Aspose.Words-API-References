---
title: Story.AppendParagraph
linktitle: AppendParagraph
articleTitle: AppendParagraph
second_title: .NET için Aspose.Words
description: Story AppendParagraph yöntemini keşfedin, kusursuz belge geliştirme için özelleştirilebilir metinle bir Paragraf nesnesini zahmetsizce oluşturun ve ekleyin.
type: docs
weight: 60
url: /tr/net/aspose.words/story/appendparagraph/
---
## Story.AppendParagraph method

Bir kısayol yöntemi oluşturan[`Paragraph`](../../paragraph/) isteğe bağlı metin içeren nesne ve bu nesnenin sonuna ekler.

```csharp
public Paragraph AppendParagraph(string text)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| text | String | Paragraf için metin. Olabilir`hükümsüz` veya boş dize. |

### Geri dönüş değeri

Yeni oluşturulan ve eklenen paragraf.

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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
