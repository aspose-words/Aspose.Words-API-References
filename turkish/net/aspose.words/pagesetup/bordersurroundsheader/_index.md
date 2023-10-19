---
title: PageSetup.BorderSurroundsHeader
linktitle: BorderSurroundsHeader
articleTitle: BorderSurroundsHeader
second_title: Aspose.Words for .NET
description: PageSetup BorderSurroundsHeader mülk. Sayfa kenarlığının üstbilgiyi içerip içermediğini veya hariç tuttuğunu belirtir C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words/pagesetup/bordersurroundsheader/
---
## PageSetup.BorderSurroundsHeader property

Sayfa kenarlığının üstbilgiyi içerip içermediğini veya hariç tuttuğunu belirtir.

```csharp
public bool BorderSurroundsHeader { get; set; }
```

## Notlar

Bu özelliğin değiştirilmesinin belgedeki tüm bölümleri etkileyeceğini unutmayın.

## Örnekler

Sayfaya ve üstbilgi/altbilgiye nasıl kenarlık uygulanacağını gösterir.

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

// Bir bölümün PageSetup nesnesi, belirleyen "BorderSurroundsHeader" ve "BorderSurroundsFooter" bayraklarına sahiptir.
// sayfa kenarlığının ana gövde metnini çevreleyip çevrelemediği, sırasıyla üstbilgi veya altbilgiyi de içerip içermediği.
// Başlığı kenarlığımızla çevrelemek için "BorderSurroundsHeader" bayrağını "true" olarak ayarlayın,
// ve ardından altbilgiyi sınırın dışında bırakacak şekilde "BorderSurroundsFooter" bayrağını ayarlayın.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
