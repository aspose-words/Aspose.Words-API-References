---
title: DocumentBuilder.MoveToSection
linktitle: MoveToSection
articleTitle: MoveToSection
second_title: .NET için Aspose.Words
description: Belge düzenleme verimliliğinizi artırmak için, herhangi bir bölümün gövdesinin başına kolayca gitmek üzere DocumentBuilder MoveToSection yöntemini keşfedin.
type: docs
weight: 610
url: /tr/net/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder.MoveToSection method

İmleci belirtilen bölümdeki gövdenin başına taşır.

```csharp
public void MoveToSection(int sectionIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sectionIndex | Int32 | Taşınılacak bölümün dizini. |

## Notlar

Ne zaman*sectionIndex*0'dan büyük veya ona eşitse, 0'ın ilk bölüm olduğu belgenin başlangıcından itibaren bir dizin belirtir.*sectionIndex* 0, değerinden küçükse, belgenin sonundan itibaren bir indeks belirtilmiş ve -1 son bölüm olarak belirlenmiştir.

İmleç, sayfanın ilk paragrafına taşınır.[`Body`](../../body/) Belirtilen bölümün.

## Örnekler

DocumentBuilder kullanılarak bir belgede üstbilgi ve altbilgilerin nasıl oluşturulacağını gösterir.

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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
