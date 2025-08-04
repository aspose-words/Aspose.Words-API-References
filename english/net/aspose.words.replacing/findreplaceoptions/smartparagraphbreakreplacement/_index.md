---
title: FindReplaceOptions.SmartParagraphBreakReplacement
linktitle: SmartParagraphBreakReplacement
articleTitle: SmartParagraphBreakReplacement
second_title: Aspose.Words for .NET
description: Discover the SmartParagraphBreakReplacement property in FindReplaceOptions. Control paragraph breaks effortlessly for seamless text formatting.
type: docs
weight: 180
url: /net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph.

The default value is `false`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

## Remarks

This option allows to replace paragraph break when there is no next sibling paragraph to which all child nodes can be moved, by finding any (not necessarily sibling) next paragraph after the paragraph being replaced.

## Examples

Shows how to remove paragraph from a table cell with a nested table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create table with paragraph and inner table in first cell.
builder.StartTable();
builder.InsertCell();
builder.Write("TEXT1");
builder.StartTable();
builder.InsertCell();
builder.EndTable();
builder.EndTable();
builder.Writeln();

FindReplaceOptions options = new FindReplaceOptions();
// When the following option is set to 'true', Aspose.Words will remove paragraph's text
// completely with its paragraph mark. Otherwise, Aspose.Words will mimic Word and remove
// only paragraph's text and leaves the paragraph mark intact (when a table follows the text).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### See Also

* class [FindReplaceOptions](../)
* namespace [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assembly [Aspose.Words](../../../)
