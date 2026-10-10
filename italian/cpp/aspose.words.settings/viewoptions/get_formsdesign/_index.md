---
title: "Aspose::Words::Settings::ViewOptions::get_FormsDesign metodo"
linktitle: "get_FormsDesign"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Settings::ViewOptions::get_FormsDesign metodo. Specifica se il documento è in modalità di progettazione dei moduli in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.settings/viewoptions/get_formsdesign/
---
## ViewOptions::get_FormsDesign method


Specifica se il documento è in modalità di progettazione dei moduli.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_FormsDesign() const
```

## Note


Attualmente funziona solo per i documenti in formato WordML.

## Esempi



Mostra come abilitare/disabilitare la modalità di progettazione dei moduli.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Imposta la proprietà "FormsDesign" su "false" per mantenere la modalità di progettazione dei moduli disabilitata.
// Imposta la proprietà "FormsDesign" su "true" per abilitare la modalità di progettazione dei moduli.
doc->get_ViewOptions()->set_FormsDesign(useFormsDesign);

doc->Save(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml");

ASPOSE_ASSERT_EQ(useFormsDesign, System::IO::File::ReadAllText(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml").Contains(u"<w:formsDesign />"));
```

## Vedi anche

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
