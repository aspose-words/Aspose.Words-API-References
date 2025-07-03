---
title: Aspose::Words::Paragraph::AppendField method
linktitle: AppendField
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Paragraph::AppendField method. Appends a field to this paragraph in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/paragraph/appendfield/
---
## Paragraph::AppendField(Aspose::Words::Fields::FieldType, bool) method


Appends a field to this paragraph.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | The type of the field to append. |
| updateField | bool | Specifies whether to update the field immediately. |

### ReturnValue

A [Field](../../../aspose.words.fields/field/) object that represents the appended field.

## Examples



Shows various ways of appending fields to a paragraph. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Below are three ways of appending a field to the end of a paragraph.
// 1 -  Append a DATE field using a field type, and then update it:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Append a TIME field using a field code:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Append a QUOTE field using a field code, and get it to display a placeholder value:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// This field will display its placeholder value until we update it.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## See Also

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&) method


Appends a field to this paragraph.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | const System::String\& | The field code to append (without curly braces). |

### ReturnValue

A [Field](../../../aspose.words.fields/field/) object that represents the appended field.

## Examples



Shows various ways of appending fields to a paragraph. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Below are three ways of appending a field to the end of a paragraph.
// 1 -  Append a DATE field using a field type, and then update it:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Append a TIME field using a field code:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Append a QUOTE field using a field code, and get it to display a placeholder value:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// This field will display its placeholder value until we update it.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## See Also

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&, const System::String\&) method


Appends a field to this paragraph.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode, const System::String &fieldValue)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | const System::String\& | The field code to append (without curly braces). |
| fieldValue | const System::String\& | The field value to append. Pass **null** for fields that do not have a value. |

### ReturnValue

A [Field](../../../aspose.words.fields/field/) object that represents the appended field.

## Examples



Shows various ways of appending fields to a paragraph. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Below are three ways of appending a field to the end of a paragraph.
// 1 -  Append a DATE field using a field type, and then update it:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Append a TIME field using a field code:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Append a QUOTE field using a field code, and get it to display a placeholder value:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// This field will display its placeholder value until we update it.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## See Also

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
