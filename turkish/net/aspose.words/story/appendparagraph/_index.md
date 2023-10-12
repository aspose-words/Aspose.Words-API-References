---
title: Story.AppendParagraph
second_title: Aspose.Words for .NET API Referansı
description: Story yöntem. Oluşturan bir kısayol yöntemiParagraph isteğe bağlı metin içeren nesneyi seçer ve onu bu nesnenin sonuna ekler.
type: docs
weight: 60
url: /tr/net/aspose.words/story/appendparagraph/
---
## Story.AppendParagraph method

Oluşturan bir kısayol yöntemi[`Paragraph`](../../paragraph/) isteğe bağlı metin içeren nesneyi seçer ve onu bu nesnenin sonuna ekler.

```csharp
public Paragraph AppendParagraph(string text)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| text | String | Paragrafın metni. Olabilir`hükümsüz` veya boş dize. |

### Geri dönüş değeri

Yeni oluşturulan ve eklenen paragraf.

### Örnekler

Üstbilgi ve altbilginin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Bir başlık oluşturun ve ona bir paragraf ekleyin. O paragraftaki metin
// bu bölümün her sayfasının üst kısmında, ana metin metninin üstünde görünecektir.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Bir altbilgi oluşturun ve ona bir paragraf ekleyin. O paragraftaki metin
// bu bölümün her sayfasının altında, ana gövde metninin altında görünecektir.
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
* ad alanı [Aspose.Words](../../story/)
* toplantı [Aspose.Words](../../../)


