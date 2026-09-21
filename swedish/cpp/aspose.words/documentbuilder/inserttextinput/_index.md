---
title: "Aspose::Words::DocumentBuilder::InsertTextInput metod"
linktitle: "InsertTextInput"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertTextInput metod. Infogar ett textformulärfält på den aktuella positionen i C++."
type: docs
weight: 49000
url: /sv/cpp/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder::InsertTextInput method


Infogar ett textformulärfält på den aktuella positionen.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertTextInput(const System::String &name, Aspose::Words::Fields::TextFormFieldType type, const System::String &format, const System::String &fieldValue, int32_t maxLength)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| namn | const System::String\& | Namnet på formulärfältet. Kan vara en tom sträng. |
| typ | Aspose::Words::Fields::TextFormFieldType | Anger typen av textformulärfältet. |
| format | const System::String\& | Formatsträng som används för att formatera värdet i formulärfältet. |
| fieldValue | const System::String\& | Text som kommer att visas i fältet. |
| maxLength | int32_t | Maximal längd som användaren kan ange i formulärfältet. Sätt till noll för obegränsad längd. |

### ReturnValue

Formulärfältets nod som just infogades.
## Anmärkningar


Om du anger ett namn för formulärfältet skapas automatiskt ett bokmärke med samma namn.

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


Visar hur man infogar ett textinmatningsformulärfält i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga ett formulär som uppmanar användaren att skriva in text.
builder->InsertTextInput(u"TextInput", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your text here", 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTextInput.docx");
```


Visar hur man infogar ett textinmatningsformulärfält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please enter text here: ");

// Infoga ett textinmatningsfält som låter användaren klicka på det och skriva in text.
// Tilldela någon platshållartext som användaren kan skriva över och skicka
// en maximal textlängd på 0 för att inte begränsa innehållet i formulärfältet.
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Formulärfältet kommer att visas som en "input"-html‑tagg med typen "text".
doc->Save(get_ArtifactsDir() + u"FormFields.TextInput.html");
```

## Se även

* Class [FormField](../../../aspose.words.fields/formfield/)
* Enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
