---
title: "Aspose::Words::Fields::TextFormFieldType enum"
linktitle: "TextFormFieldType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::TextFormFieldType enum. Anger typen av ett textformulärfält i C++."
type: docs
weight: 134000
url: /sv/cpp/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enum


Anger typen av ett textformulärfält.

```cpp
enum class TextFormFieldType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Regular | 0 | Textformulärfältet kan innehålla vilken text som helst. |
| Number | 1 | Textformulärfältet kan endast innehålla siffror. |
| Datum | 2 | Textformulärfältet kan endast innehålla ett giltigt datumvärde. |
| CurrentDate | 3 | Textformulärfältets värde är det aktuella datumet när fältet uppdateras. |
| CurrentTime | 4 | Textformulärfältets värde är den aktuella tiden när fältet uppdateras. |
| Calculated | 5 | Textformulärfältets värde beräknas från uttrycket som anges i egenskapen [TextInputDefault](../formfield/get_textinputdefault/). |


## Exempel



Visar hur man skapar formulärfält.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Formulärfält är objekt i dokumentet som användaren kan interagera med genom att bli uppmanad att ange värden.
// Vi kan skapa dem med en dokumentbyggare, och nedan finns två sätt att göra det på.
// 1 -  Grundläggande textinmatning:
builder->InsertTextInput(u"My text input", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your name here", 30);

// 2 -  Kombinationsruta med uppmaningstext och ett intervall av möjliga värden:
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"-- Select your favorite footwear --", u"Sneakers", u"Oxfords", u"Flip-flops", u"Other"});

builder->InsertParagraph();
builder->InsertComboBox(u"My combo box", items, 0);

builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateForm.docx");
```

## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
