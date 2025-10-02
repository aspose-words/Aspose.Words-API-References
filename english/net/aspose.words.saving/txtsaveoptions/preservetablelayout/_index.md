---
title: TxtSaveOptions.PreserveTableLayout
linktitle: PreserveTableLayout
articleTitle: PreserveTableLayout
second_title: Aspose.Words for .NET
description: Discover TxtSaveOptions' PreserveTableLayout feature, ensuring your tables retain their layout when saving as plain text. Enhance your document's readability!
type: docs
weight: 60
url: /net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format. The default value is `false`.

```csharp
public bool PreserveTableLayout { get; set; }
```

## Examples

Shows how to preserve the layout of tables when converting to plaintext.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1");
builder.InsertCell();
builder.Write("Row 2, cell 2");
builder.EndTable();

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Set the "PreserveTableLayout" property to "true" to apply whitespace padding to the contents
// of the output plaintext document to preserve as much of the table's layout as possible.
// Set the "PreserveTableLayout" property to "false" to save all tables' contents
// as a continuous body of text, with just a new line for each row.
txtSaveOptions.PreserveTableLayout = preserveTableLayout;

doc.Save(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
    Assert.That(docText, Is.EqualTo("Row 1, cell 1                                            Row 1, cell 2\r\n" +
                    "Row 2, cell 1                                            Row 2, cell 2\r\n\r\n"));
else
    Assert.That(docText, Is.EqualTo("Row 1, cell 1\r" +
                    "Row 1, cell 2\r" +
                    "Row 2, cell 1\r" +
                    "Row 2, cell 2\r\r\n"));
```

### See Also

* class [TxtSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
