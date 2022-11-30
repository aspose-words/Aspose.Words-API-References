---
title: get_ListName
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the name of the abstract numbering definition used for the numbering.
type: docs
weight: 27
url: /cpp/aspose.words.fields/fieldlistnum/get_listname/
---
## FieldListNum::get_ListName method


Gets or sets the name of the abstract numbering definition used for the numbering.

```cpp
System::String Aspose::Words::Fields::FieldListNum::get_ListName()
```


## Examples



Shows how to number paragraphs with LISTNUM fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// LISTNUM fields display a number that increments at each LISTNUM field.
// These fields also have a variety of options that allow us to use them to emulate numbered lists.
auto field = System::DynamicCast<FieldListNum>(builder->InsertField(FieldType::FieldListNum, true));

// Lists start counting at 1 by default, but we can set this number to a different value, such as 0.
// This field will display "0)".
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// LISTNUM fields maintain separate counts for each list level.
// Inserting a LISTNUM field in the same paragraph as another LISTNUM field
// increases the list level instead of the count.
// The next field will continue the count we started above and display a value of "1" at list level 1.
builder->InsertField(FieldType::FieldListNum, true);

// This field will start a count at list level 2. It will display a value of "1".
builder->InsertField(FieldType::FieldListNum, true);

// This field will start a count at list level 3. It will display a value of "1".
// Different list levels have different formatting,
// so these fields combined will display a value of "1)a)i)".
builder->InsertField(FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// The next LISTNUM field that we insert will continue the count at the list level
// that the previous LISTNUM field was on.
// We can use the "ListLevel" property to jump to a different list level.
// If this LISTNUM field stayed on list level 3, it would display "ii)",
// but, since we have moved it to list level 2, it carries on the count at that level and displays "b)".
field = System::DynamicCast<FieldListNum>(builder->InsertField(FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// We can set the ListName property to get the field to emulate a different AUTONUM field type.
// "NumberDefault" emulates AUTONUM, "OutlineDefault" emulates AUTONUMOUT,
// and "LegalDefault" emulates AUTONUMLGL fields.
// The "OutlineDefault" list name with 1 as the starting number will result in displaying "I.".
field = System::DynamicCast<FieldListNum>(builder->InsertField(FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// The ListName does not carry over from the previous field, so we will need to set it for each new field.
// This field continues the count with the different list name and displays "II.".
field = System::DynamicCast<FieldListNum>(builder->InsertField(FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.LISTNUM.docx");
```

## See Also

* Class [FieldListNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
