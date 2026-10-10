---
title: "Aspose::Words::Settings::ViewOptions::get_FormsDesign Methode"
linktitle: "get_FormsDesign"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::ViewOptions::get_FormsDesign Methode. Gibt an, ob das Dokument im Formular-Design‑Modus in C++ ist."
type: docs
weight: 4000
url: /de/cpp/aspose.words.settings/viewoptions/get_formsdesign/
---
## ViewOptions::get_FormsDesign method


Gibt an, ob das Dokument sich im Formular-Entwurfsmodus befindet.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_FormsDesign() const
```

## Hinweise


Derzeit funktioniert es nur für Dokumente im WordML‑Format.

## Beispiele



Zeigt, wie man den Formular-Design‑Modus aktivieren/deaktivieren kann.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Setzen Sie die Eigenschaft "FormsDesign" auf "false", um den Formular-Design‑Modus deaktiviert zu lassen.
// Setzen Sie die Eigenschaft "FormsDesign" auf "true", um den Formular-Design‑Modus zu aktivieren.
doc->get_ViewOptions()->set_FormsDesign(useFormsDesign);

doc->Save(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml");

ASPOSE_ASSERT_EQ(useFormsDesign, System::IO::File::ReadAllText(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml").Contains(u"<w:formsDesign />"));
```

## Siehe auch

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
