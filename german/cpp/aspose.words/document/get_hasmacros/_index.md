---
title: "Aspose::Words::Document::get_HasMacros Methode"
linktitle: "get_HasMacros"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_HasMacros Methode. Gibt true zurück, wenn das Dokument ein VBA-Projekt (Makros) in C++ enthält."
type: docs
weight: 30000
url: /de/cpp/aspose.words/document/get_hasmacros/
---
## Document::get_HasMacros method


Gibt **true** zurück, wenn das Dokument ein VBA‑Projekt (Makros) enthält.

```cpp
bool Aspose::Words::Document::get_HasMacros()
```


## Beispiele



Zeigt, wie MACROBUTTON-Felder verwendet werden, um die Makros eines Dokuments durch Klicken auszuführen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_TRUE(doc->get_HasMacros());

// Fügen Sie ein MACROBUTTON-Feld ein und verweisen Sie im Property MacroName per Namen auf eines der Makros des Dokuments.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"MyMacro");
field->set_DisplayText(System::String(u"Double click to run macro: ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field->GetFieldCode());

// Verwenden Sie das Property, um auf "ViewZoom200" zu verweisen, ein Makro, das mit Microsoft Word geliefert wird.
// Wir können alle anderen Makros über Ansicht -> Makros (Dropdown) -> Makros anzeigen finden.
// Wählen Sie in diesem Menü "Word Commands" aus dem Dropdown "Macros in:" aus.
// Wenn unser Dokument ein benutzerdefiniertes Makro mit demselben Namen wie ein Standardmakro enthält,
// wird unser Makro dasjenige sein, das das MACROBUTTON-Feld ausführt.
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"ViewZoom200");
field->set_DisplayText(System::String(u"Run ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  ViewZoom200 Run ViewZoom200", field->GetFieldCode());

// Speichern Sie das Dokument als makrofähigen Dokumenttyp.
doc->Save(get_ArtifactsDir() + u"Field.MACROBUTTON.docm");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
