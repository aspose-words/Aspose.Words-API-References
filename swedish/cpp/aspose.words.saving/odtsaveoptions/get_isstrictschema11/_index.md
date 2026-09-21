---
title: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11-metod"
linktitle: "get_IsStrictSchema11"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11-metod. Anger om exporten ska följa ODT-specifikationen 1.1 strikt. OOo 3.0 visar filer korrekt när de innehåller element och attribut från ODT 1.2. Använd \"false\" för detta ändamål, eller \"true\" för strikt överensstämmelse med specifikation 1.1. Standardvärdet är false i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.saving/odtsaveoptions/get_isstrictschema11/
---
## OdtSaveOptions::get_IsStrictSchema11 method


Anger om exporten ska följa ODT-specifikationen 1.1 strikt. OOo 3.0 visar filer korrekt när de innehåller element och attribut från ODT 1.2. Använd "false" för detta ändamål, eller "true" för strikt överensstämmelse med specifikation 1.1. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11() const
```


## Exempel



Visar hur man får ett sparat dokument att följa ett äldre ODT-schema.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Se även

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
