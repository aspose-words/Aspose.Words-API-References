---
title: "Aspose::Words::Settings::ViewOptions::get_FormsDesign metod"
linktitle: "get_FormsDesign"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::ViewOptions::get_FormsDesign metod. Anger om dokumentet är i formulärdesignläge i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.settings/viewoptions/get_formsdesign/
---
## ViewOptions::get_FormsDesign method


Anger om dokumentet är i formulärdesignläge.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_FormsDesign() const
```

## Anmärkningar


Fungerar för närvarande endast för dokument i WordML-format.

## Exempel



Visar hur man aktiverar/inaktiverar formulärdesignläge.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Ställ in egenskapen "FormsDesign" till "false" för att hålla formulärdesignläge inaktiverat.
// Ställ in egenskapen "FormsDesign" till "true" för att aktivera formulärdesignläge.
doc->get_ViewOptions()->set_FormsDesign(useFormsDesign);

doc->Save(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml");

ASPOSE_ASSERT_EQ(useFormsDesign, System::IO::File::ReadAllText(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml").Contains(u"<w:formsDesign />"));
```

## Se även

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
