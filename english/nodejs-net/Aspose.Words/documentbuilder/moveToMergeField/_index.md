---
title: DocumentBuilder.moveToMergeField method
linktitle: moveToMergeField method
articleTitle: moveToMergeField method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder.moveToMergeField method"
type: docs
weight: 590
url: /nodejs-net/Aspose.Words/documentbuilder/moveToMergeField/
---

## moveToMergeField(fieldName) {#string}

Moves the cursor to a position just beyond the specified merge field and removes the merge field.


```js
moveToMergeField(fieldName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldName | string | The case-insensitive name of the mail merge field. |

### Remarks

Note that this method deletes the merge field from the document after moving the cursor.




### Returns

``True`` if the merge field was found and the cursor was moved; ``False`` otherwise.


## moveToMergeField(fieldName, isAfter, isDeleteField) {#string_boolean_boolean}

Moves the merge field to the specified merge field.


```js
moveToMergeField(fieldName: stringisAfter: booleanisDeleteField: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldName | string | The case-insensitive name of the mail merge field. |
| isAfter | boolean | When ``True``, moves the cursor to be after the field end. When ``False``, moves the cursor to be before the field start.  |
| isDeleteField | boolean | When ``True``, deletes the merge field. |

### Returns

``True`` if the merge field was found and the cursor was moved; ``False`` otherwise.


## Examples

Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
// and then fill them manually.
builder.insertField(" MERGEFIELD Chairman ");
builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.moveToMergeField("Chairman");
builder.bold = true;
builder.writeln("John Doe");

builder.moveToMergeField("ChiefFinancialOfficer");
builder.italic = true;
builder.writeln("Jane Doe");

builder.moveToMergeField("ChiefTechnologyOfficer");
builder.italic = true;
builder.writeln("John Bloggs");

doc.save(base.artifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

Shows how to insert checkbox form fields into MERGEFIELDs as merge data during mail merge.

```js
test('InsertCheckBox', () => {
  let doc = new aw.Document();
  let builder = new aw.DocumentBuilder(doc);

  // Use MERGEFIELDs with "TableStart"/"TableEnd" tags to define a mail merge region
  // which belongs to a data source named "StudentCourse" and has a MERGEFIELD which accepts data from a column named "CourseName".
  builder.startTable();
  builder.insertCell();
  builder.insertField(" MERGEFIELD  TableStart:StudentCourse ");
  builder.insertCell();
  builder.insertField(" MERGEFIELD  CourseName ");
  builder.insertCell();
  builder.insertField(" MERGEFIELD  TableEnd:StudentCourse ");
  builder.endTable();

  doc.mailMerge.fieldMergingCallback = new HandleMergeFieldInsertCheckBox();

  DataTable dataTable = GetStudentCourseDataTable();

  doc.mailMerge.executeWithRegions(dataTable);
  doc.save(base.artifactsDir + "MailMergeEvent.insertCheckBox.docx");
});


  /// <summary>
  /// Upon encountering a MERGEFIELD with a specific name, inserts a check box form field instead of merge data text.
  /// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Called when a mail merge merges data into a MERGEFIELD.
    /// </summary>
  void aw.MailMerging.IFieldMergingCallback.fieldMerging(FieldMergingArgs args)
  {
    if (args.documentFieldName == "CourseName")
    {
      expect(args.tableName).toEqual("StudentCourse");

      let builder = new aw.DocumentBuilder(args.document);
      builder.moveToMergeField(args.fieldName);
      builder.insertCheckBox(args.documentFieldName + mCheckBoxCount, false, 0);

      string fieldValue = args.fieldValue.toString();

        // In this case, for every record index 'n', the corresponding field value is "Course n".
      expect(args.recordIndex).toEqual(char.GetNumericValue(fieldValue.at(7)));

      builder.write(fieldValue);
      mCheckBoxCount++;
    }
  }

  void aw.MailMerging.IFieldMergingCallback.imageFieldMerging(ImageFieldMergingArgs args)
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
  let dataTable = new DataTable("StudentCourse");
  dataTable.columns.add("CourseName");
  for (let i = 0; i < 10; i++)
  {
    DataRow datarow = dataTable.NewRow();
    dataTable.rows.add(datarow);
    datarow.at(0) = "Course " + i;
  }

  return dataTable;
}
```

Shows how to insert fields, and move the document builder's cursor to them.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.insertField("MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.insertField("MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Move the cursor to the first MERGEFIELD.
builder.moveToMergeField("MyMergeField1", true, false);

// Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
expect(builder.currentNode).toEqual(doc.range.fields.at(1).start);
expect(builder.currentNode.previousSibling).toEqual(doc.range.fields.at(0).end);

// If we wish to edit the field's field code or contents using the builder,
// its cursor would need to be inside a field.
// To place it inside a field, we would need to call the document builder's MoveTo method
// and pass the field's start or separator node as an argument.
builder.write(" Text between our merge fields. ");

doc.save(base.artifactsDir + "DocumentBuilder.MergeFields.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

