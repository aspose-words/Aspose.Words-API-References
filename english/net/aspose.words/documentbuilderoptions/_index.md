---
title: DocumentBuilderOptions Class
linktitle: DocumentBuilderOptions
articleTitle: DocumentBuilderOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.DocumentBuilderOptions class. Allows to specify additional options for the document building process in C#.
type: docs
weight: 660
url: /net/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class

Allows to specify additional options for the document building process.

```csharp
public class DocumentBuilderOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [DocumentBuilderOptions](documentbuilderoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [ContextTableFormatting](../../aspose.words/documentbuilderoptions/contexttableformatting/) { get; set; } | True if the formatting applied to table content does not affect the formatting of the content that follows it. Default value is `true`. |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
