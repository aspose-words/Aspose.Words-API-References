---
title: PageSetup.LayoutMode
linktitle: LayoutMode
articleTitle: LayoutMode
second_title: .NET için Aspose.Words
description: Belgenizin düzenini kolayca özelleştirmek için PageSetup LayoutMode özelliğini keşfedin. Esnek bölüm seçenekleriyle tasarımınızı geliştirin!
type: docs
weight: 190
url: /tr/net/aspose.words/pagesetup/layoutmode/
---
## PageSetup.LayoutMode property

Bu bölümün düzen modunu alır veya ayarlar.

```csharp
public SectionLayoutMode LayoutMode { get; set; }
```

## Örnekler

Her satırın sahip olabileceği karakter sayısının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Atışı etkinleştirin ve ardından bunu bu bölümdeki satır başına karakter sayısını ayarlamak için kullanın.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Karakter sayısı yazı tipinin boyutuna da bağlıdır.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

Her sayfanın sahip olabileceği satır sayısı için bir sınır belirlemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Atışı etkinleştirin ve ardından bunu bu bölümdeki sayfa başına satır sayısını ayarlamak için kullanın.
// Yeterince büyük bir yazı tipi boyutu, karakterlerin üst üste gelmesini önlemek için bazı satırların bir sonraki sayfaya doğru itilmesini sağlayacaktır.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Ayrıca bakınız

* enum [SectionLayoutMode](../../sectionlayoutmode/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
