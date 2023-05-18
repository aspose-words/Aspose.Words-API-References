---
title: Aspose::Words::Fields::TextFormFieldType enum
linktitle: TextFormFieldType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::TextFormFieldType enum. Specifies the type of a text form field in C++.'
type: docs
weight: 134000
url: /cpp/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enum


Specifies the type of a text form field.

```cpp
enum class TextFormFieldType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Regular | 0 | The text form field can contain any text. |
| Number | 1 | The text form field can contain only numbers. |
| Date | 2 | The text form field can contain only a valid date value. |
| CurrentDate | 3 | The text form field value is the current date when the field is updated. |
| CurrentTime | 4 | The text form field value is the current time when the field is updated. |
| Calculated | 5 | The text form field value is calculated from the expression specified in the [TextInputDefault](../formfield/get_textinputdefault/) property. |


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

## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
