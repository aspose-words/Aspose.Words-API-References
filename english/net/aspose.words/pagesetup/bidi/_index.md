---
title: PageSetup.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words for .NET
description: Discover the PageSetup Bidi property for seamless bidirectional text formatting. Enhance your documents with complex script support for better readability!
type: docs
weight: 10
url: /net/aspose.words/pagesetup/bidi/
---
## PageSetup.Bidi property

Specifies that this section contains bidirectional (complex scripts) text.

```csharp
public bool Bidi { get; set; }
```

## Remarks

When `true`, the columns in this section are laid out from right to left.

## Examples

Shows how to set the order of text columns in a section.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextColumns.SetCount(3);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 3.");

// Set the "Bidi" property to "true" to arrange the columns starting from the page's right side.
// The order of the columns will match the direction of the right-to-left text.
// Set the "Bidi" property to "false" to arrange the columns starting from the page's left side.
// The order of the columns will match the direction of the left-to-right text.
pageSetup.Bidi = reverseColumns;

doc.Save(ArtifactsDir + "PageSetup.Bidi.docx");
```

### See Also

* class [PageSetup](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
