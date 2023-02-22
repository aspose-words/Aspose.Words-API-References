---
title: MoveToMergeField
second_title: Aspose.Words for .NET API Reference
description: DocumentBuilder method. Moves the cursor to a position just beyond the specified merge field and removes the merge field in C#.
type: docs
weight: 550
url: /net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(string) {#movetomergefield}

Moves the cursor to a position just beyond the specified merge field and removes the merge field.

```csharp
public bool MoveToMergeField(string fieldName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldName | String | The case-insensitive name of the mail merge field. |

### Return Value

`true` if the merge field was found and the cursor was moved; `false` otherwise.

## Remarks

Note that this method deletes the merge field from the document after moving the cursor.

## Examples

Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
// and then fill them manually.
builder.InsertField(" MERGEFIELD Chairman ");
builder.InsertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.InsertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.MoveToMergeField("Chairman");
builder.Bold = true;
builder.Writeln("John Doe");

builder.MoveToMergeField("ChiefFinancialOfficer");
builder.Italic = true;
builder.Writeln("Jane Doe");

builder.MoveToMergeField("ChiefTechnologyOfficer");
builder.Italic = true;
builder.Writeln("John Bloggs");

doc.Save(ArtifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

Shows how to insert checkbox form fields into MERGEFIELDs as merge data during mail merge.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Use MERGEFIELDs with "TableStart"/"TableEnd" tags to define a mail merge region
    // which belongs to a data source named "StudentCourse" and has a MERGEFIELD which accepts data from a column named "CourseName".
    builder.StartTable();
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  TableStart:StudentCourse ");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  CourseName ");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  TableEnd:StudentCourse ");
    builder.EndTable();

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertCheckBox();

    DataTable dataTable = GetStudentCourseDataTable();

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMergeEvent.InsertCheckBox.docx");

/// <summary>
/// Upon encountering a MERGEFIELD with a specific name, inserts a check box form field instead of merge data text.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Called when a mail merge merges data into a MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName == "CourseName")
        {
            Assert.AreEqual("StudentCourse", args.TableName);

            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.FieldName);
            builder.InsertCheckBox(args.DocumentFieldName + mCheckBoxCount, false, 0);

            string fieldValue = args.FieldValue.ToString();

            // In this case, for every record index 'n', the corresponding field value is "Course n".
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Do nothing.
    }

    private int mCheckBoxCount;
}

/// <summary>
/// Creates a mail merge data source.
/// </summary>
private static DataTable GetStudentCourseDataTable()
{
    DataTable dataTable = new DataTable("StudentCourse");
    dataTable.Columns.Add("CourseName");
    for (int i = 0; i < 10; i++)
    {
        DataRow datarow = dataTable.NewRow();
        dataTable.Rows.Add(datarow);
        datarow[0] = "Course " + i;
    }

    return dataTable;
}
```

### See Also

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## MoveToMergeField(string, bool, bool) {#movetomergefield_1}

Moves the merge field to the specified merge field.

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldName | String | The case-insensitive name of the mail merge field. |
| isAfter | Boolean | When `true`, moves the cursor to be after the field end. When `false`, moves the cursor to be before the field start. |
| isDeleteField | Boolean | When `true`, deletes the merge field. |

### Return Value

`true` if the merge field was found and the cursor was moved; `false` otherwise.

## Examples

Shows how to insert fields, and move the document builder's cursor to them.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Move the cursor to the first MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// If we wish to edit the field's field code or contents using the builder,
// its cursor would need to be inside a field.
// To place it inside a field, we would need to call the document builder's MoveTo method
// and pass the field's start or separator node as an argument.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### See Also

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)
