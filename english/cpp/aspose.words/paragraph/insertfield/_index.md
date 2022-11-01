---
title: InsertField
second_title: Aspose.Words for C++ API Reference
description: Inserts a field into this paragraph.
type: docs
weight: 339
url: /cpp/aspose.words/paragraph/insertfield/
---
## Paragraph.InsertField(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Inserts a field into this paragraph.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | The type of the field to insert. |
| updateField | bool | Specifies whether to update the field immediately. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Reference node inside this paragraph (if refNode is null, then appends to the end of the paragraph). |
| isAfter | bool | Whether to insert the field after or before reference node. |

### ReturnValue


A [Field](../../../aspose.words.fields/field/) object that represents the inserted field.

## Examples




Shows various ways of adding fields to a paragraph. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Below are three ways of inserting a field into a paragraph.
// 1 -  Insert an AUTHOR field into a paragraph after one of the paragraph's child nodes:
auto run = MakeObject<Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ObjectExt::Box<String>(u"John Doe"));
para->InsertField(FieldType::FieldAuthor, true, run, true);

// 2 -  Insert a QUOTE field after one of the paragraph's child nodes:
run = MakeObject<Run>(doc);
run->set_Text(u".");
para->AppendChild(run);

SharedPtr<Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Insert a QUOTE field before one of the paragraph's child nodes,
// and get it to display a placeholder value:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// This field will display its placeholder value until we update it.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(ArtifactsDir + u"Paragraph.InsertField.docx");
```

## Paragraph.InsertField(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Inserts a field into this paragraph.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | const System::String\& | The field code to insert (without curly braces). |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Reference node inside this paragraph (if refNode is null, then appends to the end of the paragraph). |
| isAfter | bool | Whether to insert the field after or before reference node. |

### ReturnValue


A [Field](../../../aspose.words.fields/field/) object that represents the inserted field.

## Examples




Shows various ways of adding fields to a paragraph. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Below are three ways of inserting a field into a paragraph.
// 1 -  Insert an AUTHOR field into a paragraph after one of the paragraph's child nodes:
auto run = MakeObject<Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ObjectExt::Box<String>(u"John Doe"));
para->InsertField(FieldType::FieldAuthor, true, run, true);

// 2 -  Insert a QUOTE field after one of the paragraph's child nodes:
run = MakeObject<Run>(doc);
run->set_Text(u".");
para->AppendChild(run);

SharedPtr<Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Insert a QUOTE field before one of the paragraph's child nodes,
// and get it to display a placeholder value:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// This field will display its placeholder value until we update it.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(ArtifactsDir + u"Paragraph.InsertField.docx");
```

## Paragraph.InsertField(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Inserts a field into this paragraph.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::String &fieldValue, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | const System::String\& | The field code to insert (without curly braces). |
| fieldValue | const System::String\& | The field value to insert. Pass null for fields that do not have a value. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Reference node inside this paragraph (if refNode is null, then appends to the end of the paragraph). |
| isAfter | bool | Whether to insert the field after or before reference node. |

### ReturnValue


A [Field](../../../aspose.words.fields/field/) object that represents the inserted field.

## Examples




Shows various ways of adding fields to a paragraph. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Below are three ways of inserting a field into a paragraph.
// 1 -  Insert an AUTHOR field into a paragraph after one of the paragraph's child nodes:
auto run = MakeObject<Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ObjectExt::Box<String>(u"John Doe"));
para->InsertField(FieldType::FieldAuthor, true, run, true);

// 2 -  Insert a QUOTE field after one of the paragraph's child nodes:
run = MakeObject<Run>(doc);
run->set_Text(u".");
para->AppendChild(run);

SharedPtr<Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Insert a QUOTE field before one of the paragraph's child nodes,
// and get it to display a placeholder value:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// This field will display its placeholder value until we update it.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(ArtifactsDir + u"Paragraph.InsertField.docx");
```

