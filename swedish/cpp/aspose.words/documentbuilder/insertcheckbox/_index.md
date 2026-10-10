---
title: "Aspose::Words::DocumentBuilder::InsertCheckBox metod"
linktitle: "InsertCheckBox"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertCheckBox metod. Infogar ett kryssruteformulärfält på den aktuella positionen i C++."
type: docs
weight: 31000
url: /sv/cpp/aspose.words/documentbuilder/insertcheckbox/
---
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, int32_t) method


Infogar ett kryssruteformulärfält på den aktuella positionen.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool checkedValue, int32_t size)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| namn | const System::String\& | Namnet på formulärfältet. Kan vara en tom sträng. Värdet som är längre än 20 tecken kommer att trunkeras. |
| checkedValue | bool | Kryssstatus för kryssruteformulärfältet. |
| size | int32_t | Anger storleken på kryssrutan i punkter. Ange 0 för att låta MS Word beräkna storleken på kryssrutan automatiskt. |

### ReturnValue

Formulärfältets nod som just infogades.
## Anmärkningar


Om du anger ett namn för formulärfältet skapas automatiskt ett bokmärke med samma namn.

## Exempel



Visar hur man infogar kryssrutor i dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga kryssrutor med varierande storlekar och förinställda kryssstatusar.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// Formulärfält har en namnbegränsning på 20 tecken.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// Vi kan interagera med dessa kryssrutor i Microsoft Word genom att dubbelklicka på dem.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## Se även

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, bool, int32_t) method


Infogar ett kryssruteformulärfält på den aktuella positionen.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool defaultValue, bool checkedValue, int32_t size)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| namn | const System::String\& | Namnet på formulärfältet. Kan vara en tom sträng. Värdet som är längre än 20 tecken kommer att trunkeras. |
| defaultValue | bool | Standardvärde för kryssruteformulärfältet. |
| checkedValue | bool | Aktuell kryssstatus för kryssruteformulärfältet. |
| size | int32_t | Anger storleken på kryssrutan i punkter. Ange 0 för att låta MS Word beräkna storleken på kryssrutan automatiskt. |

### ReturnValue

Formulärfältets nod som just infogades.
## Anmärkningar


Om du anger ett namn för formulärfältet skapas automatiskt ett bokmärke med samma namn.

## Exempel



Visar hur man infogar kryssrutor i dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga kryssrutor med varierande storlekar och förinställda kryssstatusar.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// Formulärfält har en namnbegränsning på 20 tecken.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// Vi kan interagera med dessa kryssrutor i Microsoft Word genom att dubbelklicka på dem.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## Se även

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
