---
title: Field.Update
linktitle: Update
articleTitle: Update
second_title: Aspose.Words for .NET
description: Efficiently update fields with our Field Update method. Prevents conflicts by ensuring fields aren't already in use. Streamline your data management today!
type: docs
weight: 140
url: /net/aspose.words.fields/field/update/
---
## Update() {#update}

Performs the field update. Throws if the field is being updated already.

```csharp
public void Update()
```

## Examples

Shows how to insert a field into a document using FieldType.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert two fields while passing a flag which determines whether to update them as the builder inserts them.
// In some cases, updating fields could be computationally expensive, and it may be a good idea to defer the update.
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.That(doc.Range.Fields[0].GetFieldCode(), Is.EqualTo(" AUTHOR "));
Assert.That(doc.Range.Fields[1].GetFieldCode(), Is.EqualTo(" PAGE "));

if (updateInsertedFieldsImmediately)
{
    Assert.That(doc.Range.Fields[0].Result, Is.EqualTo("John Doe"));
    Assert.That(doc.Range.Fields[1].Result, Is.EqualTo("1"));
}
else
{
    Assert.That(doc.Range.Fields[0].Result, Is.EqualTo(string.Empty));
    Assert.That(doc.Range.Fields[1].Result, Is.EqualTo(string.Empty));

    // We will need to update these fields using the update methods manually.
    doc.Range.Fields[0].Update();

    Assert.That(doc.Range.Fields[0].Result, Is.EqualTo("John Doe"));

    doc.UpdateFields();

    Assert.That(doc.Range.Fields[1].Result, Is.EqualTo("1"));
}
```

Shows how to format field results.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Use a document builder to insert a field that displays a result with no format applied.
Field field = builder.InsertField("= 2 + 3");

Assert.That(field.GetFieldCode(), Is.EqualTo("= 2 + 3"));
Assert.That(field.Result, Is.EqualTo("5"));

// We can apply a format to a field's result using the field's properties.
// Below are three types of formats that we can apply to a field's result.
// 1 -  Numeric format:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo("= 2 + 3 \\# $###.00"));
Assert.That(field.Result, Is.EqualTo("$  5.00"));

// 2 -  Date/time format:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo("DATE \\@ \"dddd, MMMM dd, yyyy\""));
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 -  General format:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.That(field.GetFieldCode(), Is.EqualTo("= 25 + 33 \\* roman \\* Upper"));
Assert.That(field.Result, Is.EqualTo("LVIII"));
Assert.That(format.GeneralFormats.Count, Is.EqualTo(2));
Assert.That(format.GeneralFormats[0], Is.EqualTo(GeneralFormat.LowercaseRoman));

// We can remove our formats to revert the field's result to its original form.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.That(format.GeneralFormats.Count, Is.EqualTo(0));
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo("= 25 + 33  "));
Assert.That(field.Result, Is.EqualTo("58"));
Assert.That(format.GeneralFormats.Count, Is.EqualTo(0));
```

### See Also

* class [Field](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)

---

## Update(*bool*) {#update_1}

Performs a field update. Throws if the field is being updated already.

```csharp
public void Update(bool ignoreMergeFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| ignoreMergeFormat | Boolean | If `true` then direct field result formatting is abandoned, regardless of the MERGEFORMAT switch, otherwise normal update is performed. |

## Examples

Shows how to preserve or discard INCLUDEPICTURE fields when loading a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
    // into image shapes when loading a document that contains them.
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.That(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture), Is.True);

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.That(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture), Is.False);
    }
}
```

### See Also

* class [Field](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
