---
title: FieldListNum.HasListName
linktitle: HasListName
articleTitle: HasListName
second_title: Aspose.Words for .NET
description: Discover how the FieldListNum HasListName property indicates if an abstract numbering definition name is included in the fields code for enhanced document formatting.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldlistnum/haslistname/
---
## FieldListNum.HasListName property

Returns a value indicating whether the name of an abstract numbering definition is provided by the field's code.

```csharp
public bool HasListName { get; }
```

## Examples

Shows how to number paragraphs with LISTNUM fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// LISTNUM fields display a number that increments at each LISTNUM field.
// These fields also have a variety of options that allow us to use them to emulate numbered lists.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Lists start counting at 1 by default, but we can set this number to a different value, such as 0.
// This field will display "0)".
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.That(field.GetFieldCode(), Is.EqualTo(" LISTNUM  \\s 0"));

// LISTNUM fields maintain separate counts for each list level. 
// Inserting a LISTNUM field in the same paragraph as another LISTNUM field
// increases the list level instead of the count.
// The next field will continue the count we started above and display a value of "1" at list level 1.
builder.InsertField(FieldType.FieldListNum, true);

// This field will start a count at list level 2. It will display a value of "1".
builder.InsertField(FieldType.FieldListNum, true);

// This field will start a count at list level 3. It will display a value of "1".
// Different list levels have different formatting,
// so these fields combined will display a value of "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// The next LISTNUM field that we insert will continue the count at the list level
// that the previous LISTNUM field was on.
// We can use the "ListLevel" property to jump to a different list level.
// If this LISTNUM field stayed on list level 3, it would display "ii)",
// but, since we have moved it to list level 2, it carries on the count at that level and displays "b)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.That(field.GetFieldCode(), Is.EqualTo(" LISTNUM  \\l 2"));

// We can set the ListName property to get the field to emulate a different AUTONUM field type.
// "NumberDefault" emulates AUTONUM, "OutlineDefault" emulates AUTONUMOUT,
// and "LegalDefault" emulates AUTONUMLGL fields.
// The "OutlineDefault" list name with 1 as the starting number will result in displaying "I.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.That(field.HasListName, Is.True);
Assert.That(field.GetFieldCode(), Is.EqualTo(" LISTNUM  OutlineDefault \\s 1"));

// The ListName does not carry over from the previous field, so we will need to set it for each new field.
// This field continues the count with the different list name and displays "II.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### See Also

* class [FieldListNum](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
