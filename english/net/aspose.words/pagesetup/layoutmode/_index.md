---
title: PageSetup.LayoutMode
linktitle: LayoutMode
articleTitle: LayoutMode
second_title: Aspose.Words for .NET
description: Discover the PageSetup LayoutMode property to easily customize your document's layout. Enhance your design with flexible section options!
type: docs
weight: 190
url: /net/aspose.words/pagesetup/layoutmode/
---
## PageSetup.LayoutMode property

Gets or sets the layout mode of this section.

```csharp
public SectionLayoutMode LayoutMode { get; set; }
```

## Examples

Shows how to specify a limit for the number of lines that each page may have.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Enable pitching, and then use it to set the number of lines per page in this section.
// A large enough font size will push some lines down onto the next page to avoid overlapping characters.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

Shows how to specify a for the number of characters that each line may have.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Enable pitching, and then use it to set the number of characters per line in this section.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// The number of characters also depends on the size of the font.
doc.Styles["Normal"].Font.Size = 20;

Assert.That(doc.FirstSection.PageSetup.CharactersPerLine, Is.EqualTo(8));

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

### See Also

* enum [SectionLayoutMode](../../sectionlayoutmode/)
* class [PageSetup](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
