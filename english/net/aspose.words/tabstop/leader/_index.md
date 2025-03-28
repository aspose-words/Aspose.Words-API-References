---
title: TabStop.Leader
linktitle: Leader
articleTitle: Leader
second_title: Aspose.Words for .NET
description: Discover TabStop Leader properties to customize leader line types for your tabs, enhancing document clarity and presentation. Optimize your formatting today!
type: docs
weight: 40
url: /net/aspose.words/tabstop/leader/
---
## TabStop.Leader property

Gets or sets the type of the leader line displayed under the tab character.

```csharp
public TabLeader Leader { get; set; }
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

* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
