---
title: ImportFormatOptions Class
linktitle: ImportFormatOptions
articleTitle: ImportFormatOptions
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.ImportFormatOptions for customizable document formatting. Enhance your output with tailored import settings for optimal results.
type: docs
weight: 3690
url: /net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

Allows to specify various import options to format output.

To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/net/specify-load-options/) documentation article.

```csharp
public class ImportFormatOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [ImportFormatOptions](importformatoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [AdjustSentenceAndWordSpacing](../../aspose.words/importformatoptions/adjustsentenceandwordspacing/) { get; set; } | Gets or sets a boolean value that specifies whether to adjust sentence and word spacing automatically. The default value is `false`. |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | Gets or sets a boolean value indicating either to copy conflicting styles in KeepSourceFormatting mode. The default value is `false`. |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored if KeepSourceFormatting mode is used. The default value is `true`. |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | Gets or sets a boolean value that specifies that source formatting of textboxes content ignored if KeepSourceFormatting mode is used. The default value is `true`. |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. The default value is `false`. |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | Gets or sets a boolean value that specifies whether pasted lists will be merged with surrounding lists. The default value is `false`. |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | Gets or sets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. The default value is `false`. |

## Examples

Shows how to resolve duplicate styles while inserting documents.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
// If we insert the clone into the original document, the two styles with the same name will cause a clash.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
// Aspose.Words will resolve style clashes by converting source document styles.
// with the same names as destination styles into direct paragraph attributes.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
