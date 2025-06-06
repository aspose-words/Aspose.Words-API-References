---
title: ParagraphFormat.SnapToGrid
linktitle: SnapToGrid
articleTitle: SnapToGrid
second_title: Aspose.Words for .NET
description: Discover how the ParagraphFormat SnapToGrid property enhances layout precision by aligning your paragraphs with document grid lines for a polished look.
type: docs
weight: 300
url: /net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph.

```csharp
public bool SnapToGrid { get; set; }
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

### See Also

* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
