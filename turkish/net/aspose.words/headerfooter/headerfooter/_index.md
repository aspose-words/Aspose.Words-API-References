---
title: HeaderFooter
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: .NET için Aspose.Words
description: Sezgisel oluşturucumuzla zahmetsizce çarpıcı başlıklar ve altbilgiler tasarlayın. Benzersiz, profesyonel bir dokunuş için web sitenizin görünümünü özelleştirin!
type: docs
weight: 10
url: /tr/net/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter constructor

Belirtilen türde yeni bir üstbilgi veya altbilgi oluşturur.

```csharp
public HeaderFooter(DocumentBase doc, HeaderFooterType headerFooterType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |
| headerFooterType | HeaderFooterType | A[`HeaderFooterType`](../headerfootertype/)Başlık veya altbilginin türünü belirten value . |

## Notlar

Ne zaman[`HeaderFooter`](../) oluşturulduğunda, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve[`ParentNode`](../../node/parentnode/) dır`hükümsüz`.

Eklemek için[`HeaderFooter`](../)birine[`Section`](../../section/) kullanmak[`InsertAfter`](../../compositenode/insertafter/) ,[`InsertBefore`](../../compositenode/insertbefore/) , veya[`HeadersFooters`](../../section/headersfooters/) özellik ve yöntemler[`Add`](../../nodecollection/add/) ,[`Insert`](../../nodecollection/insert/).

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

* class [DocumentBase](../../documentbase/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
