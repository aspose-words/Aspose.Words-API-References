---
title: DocumentBuilderOptions.ContextTableFormatting
linktitle: ContextTableFormatting
articleTitle: ContextTableFormatting
second_title: Aspose.Words for .NET
description: Discover the ContextTableFormatting property in DocumentBuilderOptions. Ensure table formatting remains independent, enhancing your document's clarity and style.
type: docs
weight: 20
url: /net/aspose.words/documentbuilderoptions/contexttableformatting/
---
## DocumentBuilderOptions.ContextTableFormatting property

True if the formatting applied to table content does not affect the formatting of the content that follows it. Default value is `true`.

```csharp
public bool ContextTableFormatting { get; set; }
```

## Examples

Shows how to ignore table formatting for content after.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Adds content before the table.
// Default font size is 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Changes the font size inside the table.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// If ContextTableFormatting is true, then table formatting isn't applied to the content after.
// If ContextTableFormatting is false, then table formatting is applied to the content after.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### See Also

* class [DocumentBuilderOptions](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
