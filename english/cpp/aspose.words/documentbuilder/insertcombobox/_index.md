---
title: InsertComboBox
second_title: Aspose.Words for C++ API Reference
description: Inserts a combobox form field at the current position.
type: docs
weight: 378
url: /cpp/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder::InsertComboBox method


Inserts a combobox form field at the current position.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertComboBox(const System::String &name, const System::ArrayPtr<System::String> &items, int32_t selectedIndex)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | const System::String\& | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| items | const System::ArrayPtr\<System::String\>\& | The items of the ComboBox. Maximum is 25 items. |
| selectedIndex | int32_t | The index of the selected item in the ComboBox. |

### ReturnValue

The form field node that was just inserted.
## Remarks


If you specify a name for the form field, then a bookmark is automatically created with the same name.

## Examples



Shows how to create form fields. 
```cpp
auto builder = MakeObject<DocumentBuilder>();

// Form fields are objects in the document that the user can interact with by being prompted to enter values.
// We can create them using a document builder, and below are two ways of doing so.
// 1 -  Basic text input:
builder->InsertTextInput(u"My text input", TextFormFieldType::Regular, u"", u"Enter your name here", 30);

// 2 -  Combo box with prompt text, and a range of possible values:
ArrayPtr<String> items = MakeArray<String>({u"-- Select your favorite footwear --", u"Sneakers", u"Oxfords", u"Flip-flops", u"Other"});

builder->InsertParagraph();
builder->InsertComboBox(u"My combo box", items, 0);

builder->get_Document()->Save(ArtifactsDir + u"DocumentBuilder.CreateForm.docx");
```


Shows how to insert a combo box form field into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a form that prompts the user to pick one of the items from the menu.
builder->Write(u"Pick a fruit: ");
ArrayPtr<String> items = MakeArray<String>({u"Apple", u"Banana", u"Cherry"});
builder->InsertComboBox(u"DropDown", items, 0);

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertComboBox.docx");
```

## See Also

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
