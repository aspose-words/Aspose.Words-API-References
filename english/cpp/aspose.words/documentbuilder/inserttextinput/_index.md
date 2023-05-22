---
title: Aspose::Words::DocumentBuilder::InsertTextInput method
linktitle: InsertTextInput
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::InsertTextInput method. Inserts a text form field at the current position in C++.'
type: docs
weight: 49000
url: /cpp/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder::InsertTextInput method


Inserts a text form field at the current position.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertTextInput(const System::String &name, Aspose::Words::Fields::TextFormFieldType type, const System::String &format, const System::String &fieldValue, int32_t maxLength)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | const System::String\& | The name of the form field. Can be an empty string. |
| type | Aspose::Words::Fields::TextFormFieldType | Specifies the type of the text form field. |
| format | const System::String\& | Format string used to format the value of the form field. |
| fieldValue | const System::String\& | Text that will be shown in the field. |
| maxLength | int32_t | Maximum length the user can enter into the form field. Set to zero for unlimited length. |

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


Shows how to insert a text input form field into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a form that prompts the user to enter text.
builder->InsertTextInput(u"TextInput", TextFormFieldType::Regular, u"", u"Enter your text here", 0);

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertTextInput.docx");
```


Shows how to insert a text input form field. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Please enter text here: ");

// Insert a text input field, which will allow the user to click it and enter text.
// Assign some placeholder text that the user may overwrite and pass
// a maximum text length of 0 to apply no limit on the form field's contents.
builder->InsertTextInput(u"TextInput1", TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// The form field will appear in the form of an "input" html tag, with a type of "text".
doc->Save(ArtifactsDir + u"FormFields.TextInput.html");
```

## See Also

* Class [FormField](../../../aspose.words.fields/formfield/)
* Enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
