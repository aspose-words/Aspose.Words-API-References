---
title: DocumentBuilder.MoveToSection
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. İmleci belirtilen bir bölümde gövdenin başına taşır.
type: docs
weight: 550
url: /tr/net/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder.MoveToSection method

İmleci belirtilen bir bölümde gövdenin başına taşır.

```csharp
public void MoveToSection(int sectionIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sectionIndex | Int32 | Taşınacak bölümün dizini. |

### Notlar

SectionIndex 0'dan büyük veya 0'a eşit olduğunda, ilk bölüm 0 olmak üzere belgenin başlangıcından 'ye kadar bir dizin belirtir. partitionIndex 0, 'den küçük olduğunda, belgenin sonundan itibaren -1 son bölüm olacak şekilde bir dizin belirledi.

İmleç, satırdaki ilk paragrafa taşınır. **Gövde** belirtilen bölümden

### Örnekler

DocumentBuilder kullanılarak bir belgede nasıl üstbilgi ve altbilgi oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İlk, çift ve tek sayfalar için farklı üstbilgi ve altbilgi istediğimizi belirtin.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Başlıkları oluşturun, ardından her başlık türünü görüntülemek için belgeye üç sayfa ekleyin.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


