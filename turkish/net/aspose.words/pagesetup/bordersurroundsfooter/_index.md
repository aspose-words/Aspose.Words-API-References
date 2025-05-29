---
title: PageSetup.BorderSurroundsFooter
linktitle: BorderSurroundsFooter
articleTitle: BorderSurroundsFooter
second_title: .NET için Aspose.Words
description: PageSetup BorderSurroundsFooter özelliğinin sayfa kenarlıklarına alt bilgi eklenmesini kontrol ederek belge düzeninizi nasıl iyileştirebileceğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words/pagesetup/bordersurroundsfooter/
---
## PageSetup.BorderSurroundsFooter property

Sayfa kenarlığının altbilgiyi içerip içermediğini belirtir.

```csharp
public bool BorderSurroundsFooter { get; set; }
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
