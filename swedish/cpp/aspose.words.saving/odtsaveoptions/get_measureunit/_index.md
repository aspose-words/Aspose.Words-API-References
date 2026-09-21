---
title: "Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit-metod"
linktitle: "get_MeasureUnit"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit-metod. Tillåter att ange måttenheter som ska tillämpas på dokumentinnehållet. Standardvärdet är Centimeters i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/odtsaveoptions/get_measureunit/
---
## OdtSaveOptions::get_MeasureUnit method


Tillåter att ange måttenheter som ska tillämpas på dokumentinnehållet. Standardvärdet är [Centimeters](../../odtsavemeasureunit/)

```cpp
Aspose::Words::Saving::OdtSaveMeasureUnit Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit() const
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

* Enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
