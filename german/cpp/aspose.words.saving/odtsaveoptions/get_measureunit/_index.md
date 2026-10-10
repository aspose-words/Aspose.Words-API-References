---
title: "Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit Methode"
linktitle: "get_MeasureUnit"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit Methode. Ermöglicht die Angabe von Maßeinheiten, die auf den Dokumentinhalt angewendet werden sollen. Der Standardwert ist in C++ Zentimeter."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/odtsaveoptions/get_measureunit/
---
## OdtSaveOptions::get_MeasureUnit method


Ermöglicht das Festlegen von Maßeinheiten, die auf den Dokumentinhalt angewendet werden. Der Standardwert ist [Centimeters](../../odtsavemeasureunit/)

```cpp
Aspose::Words::Saving::OdtSaveMeasureUnit Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit() const
```


## Beispiele



Zeigt, wie ein gespeichertes Dokument an ein älteres ODT-Schema angepasst wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Siehe auch

* Enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
