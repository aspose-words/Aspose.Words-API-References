---
title: "Metodo Aspose::Words::Fields::FieldMacroButton::get_MacroName"
linktitle: "get_MacroName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldMacroButton::get_MacroName. Ottiene o imposta il nome della macro o del comando da eseguire in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.fields/fieldmacrobutton/get_macroname/
---
## FieldMacroButton::get_MacroName method


Ottiene o imposta il nome della macro o del comando da eseguire.

```cpp
System::String Aspose::Words::Fields::FieldMacroButton::get_MacroName()
```


## Esempi



Mostra come utilizzare i campi MACROBUTTON per consentirci di eseguire le macro di un documento con un clic.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_TRUE(doc->get_HasMacros());

// Inserisci un campo MACROBUTTON e fai riferimento a una delle macro del documento per nome nella proprietà MacroName.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"MyMacro");
field->set_DisplayText(System::String(u"Double click to run macro: ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field->GetFieldCode());

// Usa la proprietà per fare riferimento a "ViewZoom200", una macro fornita con Microsoft Word.
// Possiamo trovare tutte le altre macro tramite Visualizza -> Macro (menu a discesa) -> Visualizza macro.
// In quel menu, seleziona "Comandi Word" dal menu a discesa "Macro in:".
// Se il nostro documento contiene una macro personalizzata con lo stesso nome di una macro predefinita,
// la nostra macro sarà quella eseguita dal campo MACROBUTTON.
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"ViewZoom200");
field->set_DisplayText(System::String(u"Run ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  ViewZoom200 Run ViewZoom200", field->GetFieldCode());

// Salva il documento come tipo di documento abilitato alle macro.
doc->Save(get_ArtifactsDir() + u"Field.MACROBUTTON.docm");
```

## Vedi anche

* Class [FieldMacroButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
