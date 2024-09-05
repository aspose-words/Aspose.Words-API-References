---
title: FieldStyleRef Class
linktitle: FieldStyleRef
articleTitle: FieldStyleRef
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldStyleRef class. Implements the STYLEREF field in C#.
type: docs
weight: 2700
url: /net/aspose.words.fields/fieldstyleref/
---
## FieldStyleRef class

Implements the STYLEREF field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldStyleRef : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldStyleRef](fieldstyleref/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end/) { get; } | Gets the node that represents the field end. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Gets a [`FieldFormat`](../fieldformat/) object that provides typed access to field's formatting. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldstyleref/insertparagraphnumber/) { get; set; } | Gets or sets whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinfullcontext/) { get; set; } | Gets or sets whether to insert the paragraph number of the referenced paragraph in full context. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinrelativecontext/) { get; set; } | Gets or sets whether to insert the paragraph number of the referenced paragraph in relative context. |
| [InsertRelativePosition](../../aspose.words.fields/fieldstyleref/insertrelativeposition/) { get; set; } | Gets or sets whether to insert the relative position of the referenced paragraph. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Gets or sets the LCID of the field. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [SearchFromBottom](../../aspose.words.fields/fieldstyleref/searchfrombottom/) { get; set; } | Gets or sets whether to search from the bottom of the current page, rather from the top. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Gets the node that represents the field separator. Can be `null`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Gets the node that represents the start of the field. |
| [StyleName](../../aspose.words.fields/fieldstyleref/stylename/) { get; set; } | Gets or sets the name of the style by which the text to search for is formatted. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldstyleref/suppressnondelimiters/) { get; set; } | Gets or sets whether to suppress non-delimiter characters. |
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

The STYLEREF is used to reference a fragment of text within the document that is formatted with the specified style.

## Examples

Shows how to use STYLEREF fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a list based using a Microsoft Word list template.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// This generated list will display "1.a )".
// Space before the bracket is a non-delimiter character, which we can suppress. 
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// Add text and apply paragraph styles that STYLEREF fields will reference.
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Place a STYLEREF field in the header and display the first "List Paragraph"-styled text in the document.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// Place a STYLEREF field in the footer, and have it display the last text.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// We can also use STYLEREF fields to reference the list numbers of lists.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
