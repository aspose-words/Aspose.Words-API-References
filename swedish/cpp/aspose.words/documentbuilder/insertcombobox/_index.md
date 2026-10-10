---
title: "Aspose::Words::DocumentBuilder::InsertComboBox metod"
linktitle: "InsertComboBox"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertComboBox metod. Infogar ett combobox-formulärfält på den aktuella positionen i C++."
type: docs
weight: 32000
url: /sv/cpp/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder::InsertComboBox method


Infogar ett kombinationsruteformulärfält på den aktuella positionen.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertComboBox(const System::String &name, const System::ArrayPtr<System::String> &items, int32_t selectedIndex)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| namn | const System::String\& | Namnet på formulärfältet. Kan vara en tom sträng. Värdet som är längre än 20 tecken kommer att trunkeras. |
| objekt | const System::ArrayPtr\<System::String\>\& | Objekten i ComboBoxen. Maximalt är 25 objekt. |
| selectedIndex | int32_t | Indexet för det valda objektet i ComboBoxen. |

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


Visar hur man infogar ett kombinationsruta-formulärfält i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga ett formulär som uppmanar användaren att välja ett av objekten i menyn.
builder->Write(u"Pick a fruit: ");
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"});
builder->InsertComboBox(u"DropDown", items, 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertComboBox.docx");
```

## Se även

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
