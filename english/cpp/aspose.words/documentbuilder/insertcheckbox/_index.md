---
title: Aspose::Words::DocumentBuilder::InsertCheckBox method
linktitle: InsertCheckBox
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::InsertCheckBox method. Inserts a checkbox form field at the current position in C++.'
type: docs
weight: 31000
url: /cpp/aspose.words/documentbuilder/insertcheckbox/
---
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, int32_t) method


Inserts a checkbox form field at the current position.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool checkedValue, int32_t size)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | const System::String\& | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| checkedValue | bool | Checked status of the checkbox form field. |
| size | int32_t | Specifies the size of the checkbox in points. Specify 0 for MS Word to calculate the size of the checkbox automatically. |

### ReturnValue

The form field node that was just inserted.
## Remarks


If you specify a name for the form field, then a bookmark is automatically created with the same name.

## Examples



Shows how to insert checkboxes into the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert checkboxes of varying sizes and default checked statuses.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// Form fields have a name length limit of 20 characters.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// We can interact with these check boxes in Microsoft Word by double clicking them.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## See Also

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, bool, int32_t) method


Inserts a checkbox form field at the current position.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool defaultValue, bool checkedValue, int32_t size)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | const System::String\& | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| defaultValue | bool | Default value of the checkbox form field. |
| checkedValue | bool | Current checked status of the checkbox form field. |
| size | int32_t | Specifies the size of the checkbox in points. Specify 0 for MS Word to calculate the size of the checkbox automatically. |

### ReturnValue

The form field node that was just inserted.
## Remarks


If you specify a name for the form field, then a bookmark is automatically created with the same name.

## Examples



Shows how to insert checkboxes into the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert checkboxes of varying sizes and default checked statuses.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// Form fields have a name length limit of 20 characters.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// We can interact with these check boxes in Microsoft Word by double clicking them.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## See Also

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
