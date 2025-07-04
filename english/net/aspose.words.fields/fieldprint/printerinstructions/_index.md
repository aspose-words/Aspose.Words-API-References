---
title: FieldPrint.PrinterInstructions
linktitle: PrinterInstructions
articleTitle: PrinterInstructions
second_title: Aspose.Words for .NET
description: Discover how to manage printer-specific control codes and PostScript instructions with FieldPrint PrinterInstructions for optimized printing solutions.
type: docs
weight: 30
url: /net/aspose.words.fields/fieldprint/printerinstructions/
---
## FieldPrint.PrinterInstructions property

Gets or sets the printer-specific control code characters or PostScript instructions.

```csharp
public string PrinterInstructions { get; set; }
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
