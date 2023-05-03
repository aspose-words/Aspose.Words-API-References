---
title: TabStop Class
linktitle: TabStop
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.TabStop class. Represents a single custom tab stop. The TabStop object is a member of the TabStopCollection collection in C#.
type: docs
weight: 6100
url: /net/aspose.words/tabstop/
---
## TabStop class

Represents a single custom tab stop. The `TabStop` object is a member of the [`TabStopCollection`](../tabstopcollection/) collection.

To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article.

```csharp
public sealed class TabStop
```

## Constructors

| Name | Description |
| --- | --- |
| [TabStop](tabstop/#constructor)(*double*) | Initializes a new instance of this class. |
| [TabStop](tabstop/#constructor_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Initializes a new instance of this class. |

## Properties

| Name | Description |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | Gets or sets the alignment of text at this tab stop. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | Returns `true` if this tab stop clears any existing tab stops in this position. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | Gets or sets the type of the leader line displayed under the tab character. |
| [Position](../../aspose.words/tabstop/position/) { get; } | Gets the position of the tab stop in points. |

## Methods

| Name | Description |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(*TabStop*) | Compares with the specified `TabStop`. |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | Calculates hash code for this object. |

## Remarks

Normally, a tab stop specifies a position where a tab stop exists. But because tab stops can be inherited from parent styles, it might be needed for the child object to define explicitly that there is no tab stop at a given position. To clear an inherited tab stop at a given position, create a `TabStop` object and set [`Alignment`](./alignment/) to Clear.

For more information see [`TabStopCollection`](../tabstopcollection/).

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
