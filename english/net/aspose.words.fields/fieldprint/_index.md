---
title: FieldPrint Class
linktitle: FieldPrint
articleTitle: FieldPrint
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldPrint class. Implements the PRINT field in C#.
type: docs
weight: 2670
url: /net/aspose.words.fields/fieldprint/
---
## FieldPrint class

Implements the PRINT field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldPrint : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldPrint](fieldprint/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end/) { get; } | Gets the node that represents the field end. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Gets a [`FieldFormat`](../fieldformat/) object that provides typed access to field's formatting. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Gets or sets the LCID of the field. |
| [PostScriptGroup](../../aspose.words.fields/fieldprint/postscriptgroup/) { get; set; } | Gets or sets the drawing rectangle that the PostScript instructions operate on. |
| [PrinterInstructions](../../aspose.words.fields/fieldprint/printerinstructions/) { get; set; } | Gets or sets the printer-specific control code characters or PostScript instructions. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Gets the node that represents the field separator. Can be `null`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Gets the node that represents the start of the field. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Gets the Microsoft Word field type. |

## Methods

| Name | Description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../../aspose.words.fields/field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns `null`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Performs a field update. Throws if the field is being updated already. |

## Remarks

An instruction to send the printer-specific control code characters to the selected printer when the document is printed.

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

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
