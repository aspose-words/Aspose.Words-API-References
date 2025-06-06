---
title: TabStop.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words for .NET
description: Discover the TabStop Alignment property to easily customize text alignment at tab stops, enhancing your document's layout and readability.
type: docs
weight: 20
url: /net/aspose.words/tabstop/alignment/
---
## TabStop.Alignment property

Gets or sets the alignment of text at this tab stop.

```csharp
public TabAlignment Alignment { get; set; }
```

## Examples

Shows how to modify the position of the right tab stop in TOC related paragraphs.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Replace the first default tab, stop with a custom tab stop.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### See Also

* enum [TabAlignment](../../tabalignment/)
* class [TabStop](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
