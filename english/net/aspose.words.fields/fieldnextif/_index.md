---
title: FieldNextIf Class
linktitle: FieldNextIf
articleTitle: FieldNextIf
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fields.FieldNextIf class—efficiently implement NEXTIF fields to enhance document automation and streamline your workflows.
type: docs
weight: 2600
url: /net/aspose.words.fields/fieldnextif/
---
## FieldNextIf class

Implements the NEXTIF field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldNextIf : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldNextIf](fieldnextif/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldnextif/comparisonoperator/) { get; set; } | Gets or sets the comparison operator. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end/) { get; } | Gets the node that represents the field end. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Gets a [`FieldFormat`](../fieldformat/) object that provides typed access to field's formatting. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LeftExpression](../../aspose.words.fields/fieldnextif/leftexpression/) { get; set; } | Gets or sets the left part of the comparison expression. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Gets or sets the LCID of the field. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [RightExpression](../../aspose.words.fields/fieldnextif/rightexpression/) { get; set; } | Gets or sets the right part of the comparison expression. |
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

Compares the values designated by the expressions [`LeftExpression`](./leftexpression/) and [`RightExpression`](./rightexpression/) in comparison using the operator designated by [`ComparisonOperator`](./comparisonoperator/). If the comparison is true, the next data record is merged into the current merge document. (Merge fields that follow the NEXTIF in the main document are replaced by values from the next data record rather than the current data record.) If the comparison is false, the next data record is merged into a new merge document.

## Examples

Shows how to use NEXT/NEXTIF fields to merge multiple rows into one page during a mail merge.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Create a data source for our mail merge with 3 rows.
    // A mail merge that uses this table would normally create a 3-page document.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // If we have multiple merge fields with the same FieldName,
    // they will receive data from the same row of the data source and display the same value after the merge.
    // A NEXT field tells the mail merge instantly to move down one row,
    // which means any MERGEFIELDs that follow the NEXT field will receive data from the next row.
    // Make sure never to try to skip to the next row while already on the last row.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // After the merge, the data source values that these MERGEFIELDs accept
    // will end up on the same page as the MERGEFIELDs above. 
    InsertMergeFields(builder, "Second row: ");

    // A NEXTIF field has the same function as a NEXT field,
    // but it skips to the next row only if a statement constructed by the following 3 properties is true.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // If the comparison asserted by the above field is correct,
    // the following 3 merge fields will take data from the third row.
    // Otherwise, these fields will take data from row 2 again.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

    // Our data source has 3 rows, and we skipped rows twice. 
    // Our output document will have 1 page with data from all 3 rows.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// Uses a document builder to insert MERGEFIELDs for a data source that contains columns named "Courtesy Title", "First Name" and "Last Name".
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// Uses a document builder to insert a MERRGEFIELD with specified properties.
/// </summary>
public void InsertMergeField(DocumentBuilder builder, string fieldName, string textBefore, string textAfter)
{
    FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, true);
    field.FieldName = fieldName;
    field.TextBefore = textBefore;
    field.TextAfter = textAfter;
}
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
