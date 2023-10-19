---
title: PageSetup.LayoutMode
linktitle: LayoutMode
articleTitle: LayoutMode
second_title: Aspose.Words for .NET
description: PageSetup LayoutMode mülk. Bu bölümün düzen modunu alır veya ayarlar C#'da.
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

Her satırın sahip olabileceği karakter sayısı için nasıl belirtileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Perdelemeyi etkinleştirin ve ardından bu bölümde satır başına karakter sayısını ayarlamak için bunu kullanın.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Karakter sayısı aynı zamanda yazı tipinin boyutuna da bağlıdır.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

Her sayfanın sahip olabileceği satır sayısına ilişkin sınırın nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Perdelemeyi etkinleştirin ve ardından bu bölümdeki sayfa başına satır sayısını ayarlamak için bunu kullanın.
// Yeterince büyük bir yazı tipi boyutu, karakterlerin çakışmasını önlemek için bazı satırları sonraki sayfaya doğru itecektir.
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
