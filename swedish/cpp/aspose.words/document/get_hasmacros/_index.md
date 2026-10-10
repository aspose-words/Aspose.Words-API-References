---
title: "Aspose::Words::Document::get_HasMacros metod"
linktitle: "get_HasMacros"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_HasMacros metod. Returnerar true om dokumentet har ett VBA-projekt (makron) i C++."
type: docs
weight: 30000
url: /sv/cpp/aspose.words/document/get_hasmacros/
---
## Document::get_HasMacros method


Returnerar **true** om dokumentet har ett VBA‑projekt (makron).

```cpp
bool Aspose::Words::Document::get_HasMacros()
```


## Exempel



Visar hur man använder MACROBUTTON-fält för att låta oss köra ett dokuments makron genom att klicka.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_TRUE(doc->get_HasMacros());

// Infoga ett MACROBUTTON-fält och referera till ett av dokumentets makron med namn i egenskapen MacroName.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"MyMacro");
field->set_DisplayText(System::String(u"Double click to run macro: ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field->GetFieldCode());

// Använd egenskapen för att referera till "ViewZoom200", ett makro som levereras med Microsoft Word.
// Vi kan hitta alla andra makron via Visa -> Makron (rullgardinsmeny) -> Visa Makron.
// I den menyn, välj "Word Commands" från rullgardinsmenyn "Macros in:".
// Om vårt dokument innehåller ett anpassat makro med samma namn som ett standardmakro,
// kommer vårt makro att vara det som MACROBUTTON-fältet kör.
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"ViewZoom200");
field->set_DisplayText(System::String(u"Run ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  ViewZoom200 Run ViewZoom200", field->GetFieldCode());

// Spara dokumentet som en makroaktiverad dokumenttyp.
doc->Save(get_ArtifactsDir() + u"Field.MACROBUTTON.docm");
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
