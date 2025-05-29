---
title: PageSetup.BorderSurroundsHeader
linktitle: BorderSurroundsHeader
articleTitle: BorderSurroundsHeader
second_title: .NET için Aspose.Words
description: Sayfa kenarlıklarınızı özelleştirmek için PageSetup BorderSurroundsHeader özelliğini keşfedin. Cilalı bir belge düzeni için başlık eklemeyi kontrol edin.
type: docs
weight: 70
url: /tr/net/aspose.words/pagesetup/bordersurroundsheader/
---
## PageSetup.BorderSurroundsHeader property

Sayfa kenarlığının başlığı içerip içermediğini belirtir.

```csharp
public bool BorderSurroundsHeader { get; set; }
```

## Notlar

Bu özelliği değiştirmenin belgedeki tüm bölümleri etkileyeceğini unutmayın.

## Örnekler

Sayfaya ve üstbilgi/altbilgiye kenarlık eklemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

// Mavi çift çizgili bir kenarlık ekleyin.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// Bir bölümün PageSetup nesnesi, bölümün PageSetup'ını belirleyen "BorderSurroundsHeader" ve "BorderSurroundsFooter" bayraklarına sahiptir.
// bir sayfa kenarlığının ana gövde metnini çevreleyip çevrelemediği, ayrıca sırasıyla üstbilgi veya altbilgiyi de içerdiği.
// Başlığı kenarlığımızla çevrelemek için "BorderSurroundsHeader" bayrağını "true" olarak ayarlayın,
// ve ardından altbilgiyi sınırın dışında bırakmak için "BorderSurroundsFooter" bayrağını ayarlayın.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
