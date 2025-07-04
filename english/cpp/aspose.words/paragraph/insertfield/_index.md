---
title: Aspose::Words::Paragraph::InsertField method
linktitle: InsertField
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Paragraph::InsertField method. Inserts a field into this paragraph in C++.'
type: docs
weight: 29000
url: /cpp/aspose.words/paragraph/insertfield/
---
## Paragraph::InsertField(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Inserts a field into this paragraph.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | The type of the field to insert. |
| updateField | bool | Specifies whether to update the field immediately. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Reference node inside this paragraph (if *refNode* is **null**, then appends to the end of the paragraph). |
| isAfter | bool | Whether to insert the field after or before reference node. |

### ReturnValue

A [Field](../../../aspose.words.fields/field/) object that represents the inserted field.

## Examples



Shows various ways of adding fields to a paragraph. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Below are three ways of inserting a field into a paragraph.
// 1 -  Insert an AUTHOR field into a paragraph after one of the paragraph's child nodes:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Insert a QUOTE field after one of the paragraph's child nodes:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Insert a QUOTE field before one of the paragraph's child nodes,
// and get it to display a placeholder value:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// This field will display its placeholder value until we update it.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## See Also

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Inserts a field into this paragraph.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | const System::String\& | The field code to insert (without curly braces). |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Reference node inside this paragraph (if *refNode* is **null**, then appends to the end of the paragraph). |
| isAfter | bool | Whether to insert the field after or before reference node. |

### ReturnValue

A [Field](../../../aspose.words.fields/field/) object that represents the inserted field.

## Examples



Shows various ways of adding fields to a paragraph. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Below are three ways of inserting a field into a paragraph.
// 1 -  Insert an AUTHOR field into a paragraph after one of the paragraph's child nodes:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Insert a QUOTE field after one of the paragraph's child nodes:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Insert a QUOTE field before one of the paragraph's child nodes,
// and get it to display a placeholder value:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// This field will display its placeholder value until we update it.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## See Also

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Inserts a field into this paragraph.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::String &fieldValue, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | const System::String\& | The field code to insert (without curly braces). |
| fieldValue | const System::String\& | The field value to insert. Pass **null** for fields that do not have a value. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Reference node inside this paragraph (if *refNode* is **null**, then appends to the end of the paragraph). |
| isAfter | bool | Whether to insert the field after or before reference node. |

### ReturnValue

A [Field](../../../aspose.words.fields/field/) object that represents the inserted field.

## Examples



Shows various ways of adding fields to a paragraph. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Below are three ways of inserting a field into a paragraph.
// 1 -  Insert an AUTHOR field into a paragraph after one of the paragraph's child nodes:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Insert a QUOTE field after one of the paragraph's child nodes:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Insert a QUOTE field before one of the paragraph's child nodes,
// and get it to display a placeholder value:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// This field will display its placeholder value until we update it.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## See Also

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
