---
title: FieldPrint.PostScriptGroup
linktitle: PostScriptGroup
articleTitle: PostScriptGroup
second_title: Aspose.Words for .NET
description: Discover the FieldPrint PostScriptGroup property to easily manage your drawing rectangle for efficient PostScript instruction handling.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldprint/postscriptgroup/
---
## FieldPrint.PostScriptGroup property

Gets or sets the drawing rectangle that the PostScript instructions operate on.

```csharp
public string PostScriptGroup { get; set; }
```

## Examples

Shows to insert a PRINT field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// The PRINT field can send instructions to the printer.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// Set the area for the printer to perform instructions over.
// In this case, it will be the paragraph that contains our PRINT field.
field.PostScriptGroup = "para";

// When we use a printer that supports PostScript to print our document,
// this command will turn the entire area that we specified in "field.PostScriptGroup" white.
field.PrinterInstructions = "erasepage";

Assert.That(field.GetFieldCode(), Is.EqualTo(" PRINT  erasepage \\p para"));

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### See Also

* class [FieldPrint](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
