---
title: Style.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words for .NET API Reference
description: Style StyleIdentifier property. Gets the locale independent style identifier for a builtin style in C#.
type: docs
weight: 150
url: /net/aspose.words/style/styleidentifier/
---
## Style.StyleIdentifier property

Gets the locale independent style identifier for a built-in style.

```csharp
public StyleIdentifier StyleIdentifier { get; }
```

## Remarks

For user defined (custom) styles, this property returns User.

## Examples

Shows how to modify the position of the right tab stop in TOC related paragraphs.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
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

* enum [StyleIdentifier](../../styleidentifier/)
* class [Style](../)
* namespace [Aspose.Words](../../style/)
* assembly [Aspose.Words](../../../)
