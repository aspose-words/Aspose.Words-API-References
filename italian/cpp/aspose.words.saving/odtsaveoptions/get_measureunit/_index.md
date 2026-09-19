---
title: "Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit method"
linktitle: "get_MeasureUnit"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit method. Consente di specificare le unità di misura da applicare al contenuto del documento. Il valore predefinito è Centimeters in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/odtsaveoptions/get_measureunit/
---
## OdtSaveOptions::get_MeasureUnit method


Consente di specificare le unità di misura da applicare al contenuto del documento. Il valore predefinito è [Centimeters](../../odtsavemeasureunit/)

```cpp
Aspose::Words::Saving::OdtSaveMeasureUnit Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit() const
```


## Esempi



Mostra come far conformare un documento salvato a uno schema ODT più vecchio.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Vedi anche

* Enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
