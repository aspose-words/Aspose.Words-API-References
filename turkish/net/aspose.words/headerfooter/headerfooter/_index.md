---
title: HeaderFooter.HeaderFooter
second_title: Aspose.Words for .NET API Referansı
description: HeaderFooter inşaatçı. Belirtilen türde yeni bir üstbilgi veya altbilgi oluşturur.
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
| headerFooterType | HeaderFooterType | A[`HeaderFooterType`](../headerfootertype/)üst bilgi veya alt bilgi türünü belirten value . |

### Notlar

Ne zaman **Üstbilgi Altbilgi** oluşturulur, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değil ve **Üst Düğüm** boş.

Eklemek **Üstbilgi Altbilgi** bir **Bölüm** Section.InsertAfter, Section.InsertBefore, HeadersFooters.Add veya HeadersFooters.Insert'i kullanın.

### Örnekler

Üstbilgi ve altbilginin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Bir başlık oluşturun ve ona bir paragraf ekleyin. O paragraftaki metin
// bu bölümün her sayfasının başında, ana gövde metninin üstünde görünecektir.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Bir alt bilgi oluşturun ve ona bir paragraf ekleyin. O paragraftaki metin
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
* ad alanı [Aspose.Words](../../headerfooter/)
* toplantı [Aspose.Words](../../../)


