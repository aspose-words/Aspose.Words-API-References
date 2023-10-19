---
title: HeaderFooter
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: Aspose.Words for .NET
description: HeaderFooter inşaatçı. Belirtilen türde yeni bir üst bilgi veya alt bilgi oluşturur C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter constructor

Belirtilen türde yeni bir üst bilgi veya alt bilgi oluşturur.

```csharp
public HeaderFooter(DocumentBase doc, HeaderFooterType headerFooterType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahibi belgesi. |
| headerFooterType | HeaderFooterType | A[`HeaderFooterType`](../headerfootertype/) üstbilgi veya altbilginin türünü belirten value . |

## Notlar

Ne zaman[`HeaderFooter`](../) oluşturulduysa, belirtilen belgeye aittir ancak henüz değildir ve belgenin bir parçası değildir ve[`ParentNode`](../../node/parentnode/) dır-dir`hükümsüz`.

Eklemek[`HeaderFooter`](../)bir[`Section`](../../section/) kullanmak[`InsertAfter`](../../compositenode/insertafter/) ,[`InsertBefore`](../../compositenode/insertbefore/) , veya[`HeadersFooters`](../../section/headersfooters/) özellik ve yöntemler[`Add`](../../nodecollection/add/) ,[`Insert`](../../nodecollection/insert/).

## Örnekler

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

* class [DocumentBase](../../documentbase/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
