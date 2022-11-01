---
title: InsertField
second_title: Aspose.Words for C++ API Reference
description: Inserts a Word field into a document and optionally updates the field result.
type: docs
weight: 404
url: /cpp/aspose.words/documentbuilder/insertfield/
---
## DocumentBuilder.InsertField(Aspose::Words::Fields::FieldType, bool) method


Inserts a Word field into a document and optionally updates the field result.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | The type of the field to append. |
| updateField | bool | Specifies whether to update the field immediately. |

### ReturnValue


A [Field](../../../aspose.words.fields/field/) object that represents the inserted field.

This method inserts a field into a document. Aspose.Words can update fields of most types, but not all. For more details see the **InsertField()** overload.

## Examples




Shows how to insert a field into a document using FieldType. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert two fields while passing a flag which determines whether to update them as the builder inserts them.
// In some cases, updating fields could be computationally expensive, and it may be a good idea to defer the update.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
builder->Write(u"This document was written by ");
builder->InsertField(FieldType::FieldAuthor, updateInsertedFieldsImmediately);

builder->InsertParagraph();
builder->Write(u"\nThis is page ");
builder->InsertField(FieldType::FieldPage, updateInsertedFieldsImmediately);

ASSERT_EQ(u" AUTHOR ", doc->get_Range()->get_Fields()->idx_get(0)->GetFieldCode());
ASSERT_EQ(u" PAGE ", doc->get_Range()->get_Fields()->idx_get(1)->GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
else
{
    ASSERT_EQ(String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

    // We will need to update these fields using the update methods manually.
    doc->get_Range()->get_Fields()->idx_get(0)->Update();

    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

    doc->UpdateFields();

    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
```

## DocumentBuilder.InsertField(const System::String\&) method


Inserts a Word field into a document and updates the field result.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | const System::String\& | The field code to insert (without curly braces). |

### ReturnValue


A [Field](../../../aspose.words.fields/field/) object that represents the inserted field.

This method inserts a field into a document and updates the field result immediately. Aspose.Words can update fields of most types, but not all. For more details see the **InsertField()** overload.

## Examples




Shows how to insert fields, and move the document builder's cursor to them. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
builder->InsertField(u"MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

// Move the cursor to the first MERGEFIELD.
builder->MoveToMergeField(u"MyMergeField1", true, false);

// Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Start(), builder->get_CurrentNode());
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_End(), builder->get_CurrentNode()->get_PreviousSibling());

// If we wish to edit the field's field code or contents using the builder,
// its cursor would need to be inside a field.
// To place it inside a field, we would need to call the document builder's MoveTo method
// and pass the field's start or separator node as an argument.
builder->Write(u" Text between our merge fields. ");

doc->Save(ArtifactsDir + u"DocumentBuilder.MergeFields.docx");
```


Shows how to insert a field into a document using a field code. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// This overload of the InsertField method automatically updates inserted fields.
ASSERT_LE(System::Math::Abs((System::DateTime::Parse(field->get_Result()) - System::DateTime::get_Today()).get_Hours()), 24);
```

## DocumentBuilder.InsertField(const System::String\&, const System::String\&) method


Inserts a Word field into a document without updating the field result.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode, const System::String &fieldValue)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | const System::String\& | The field code to insert (without curly braces). |
| fieldValue | const System::String\& | The field value to insert. Pass null for fields that do not have a value. |

### ReturnValue


A [Field](../../../aspose.words.fields/field/) object that represents the inserted field.

[Fields](../../../aspose.words.fields/) in Microsoft Word documents consist of a field code and a field result. The field code is like a formula and the field result is like the value that the formula produces. The field code may also contain field switches that are like additional instructions to perform a specific action.

You can switch between displaying field codes and results in your document in Microsoft Word using the keyboard shortcut Alt+F9. Field codes appear between curly braces ( { } ).

To create a field, you need to specify a field type, field code and a "placeholder" field value. If you are not sure about a particular field code syntax, create the field in Microsoft Word first and switch to see its field code.

Aspose.Words can calculate field results for most of the field types, but this method does not update the field result automatically. Because the field result is not calculated automatically, you are expected to pass some string value (or even an empty string) that will be inserted into the field result. This value will remain in the field result as a placeholder until the field is updated. To update the field result you can call [Update](../../../aspose.words.fields/field/update/) on the field object returned to you or [UpdateFields](../../document/updatefields/) to update fields in the whole document.

## Examples




Shows how to set up page numbering in a section. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// Move the document builder to the first section's primary header,
// which every page in that section will display.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);

// Insert a PAGE field, which will display the number of the current page.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Configure the section to have the page count that PAGE fields display start from 5.
// Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
SharedPtr<PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(NumberStyle::UppercaseRoman);

// Create another primary header for the second section, with another PAGE field.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Configure the section to have the page count that PAGE fields display start from 10.
// Also, configure all PAGE fields to display their page numbers using Arabic numbers.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(NumberStyle::Arabic);

doc->Save(ArtifactsDir + u"PageSetup.PageNumbering.docx");
```

