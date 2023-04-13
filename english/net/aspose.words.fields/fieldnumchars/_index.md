---
title: FieldNumChars Class
linktitle: FieldNumChars
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Fields.FieldNumChars class. Implements the NUMCHARS field in C#.
type: docs
weight: 2100
url: /net/aspose.words.fields/fieldnumchars/
---
## FieldNumChars class

Implements the NUMCHARS field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldNumChars : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldNumChars](fieldnumchars/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end/) { get; } | Gets the node that represents the field end. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Gets a [`FieldFormat`](../fieldformat/) object that provides typed access to field's formatting. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Gets or sets the LCID of the field. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Gets the node that represents the field separator. Can be `null`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Gets the node that represents the start of the field. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Gets the Microsoft Word field type. |

## Methods

| Name | Description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../../aspose.words.fields/field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns `null`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Remarks

Retrieves the number of characters in the current document, as recorded in the **Characters** property of the built-in document properties.

## Examples

Shows how to use NUMCHARS, NUMWORDS, NUMPAGES and PAGE fields to track the size of our documents.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Below are three types of fields that we can use to track the size of our documents.
// 1 -  Track the character count with a NUMCHARS field:
FieldNumChars fieldNumChars = (FieldNumChars)builder.InsertField(FieldType.FieldNumChars, true);       
builder.Writeln(" characters");

// 2 -  Track the word count with a NUMWORDS field:
FieldNumWords fieldNumWords = (FieldNumWords)builder.InsertField(FieldType.FieldNumWords, true);
builder.Writeln(" words");

// 3 -  Use both PAGE and NUMPAGES fields to display what page the field is on,
// and the total number of pages in the document:
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Page ");
FieldPage fieldPage = (FieldPage)builder.InsertField(FieldType.FieldPage, true);
builder.Write(" of ");
FieldNumPages fieldNumPages = (FieldNumPages)builder.InsertField(FieldType.FieldNumPages, true);

Assert.AreEqual(" NUMCHARS ", fieldNumChars.GetFieldCode());
Assert.AreEqual(" NUMWORDS ", fieldNumWords.GetFieldCode());
Assert.AreEqual(" NUMPAGES ", fieldNumPages.GetFieldCode());
Assert.AreEqual(" PAGE ", fieldPage.GetFieldCode());

// These fields will not maintain accurate values in real time
// while we edit the document programmatically using Aspose.Words, or in Microsoft Word.
// We need to update them every we need to see an up-to-date value. 
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.NUMCHARS.NUMWORDS.NUMPAGES.PAGE.docx");
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
