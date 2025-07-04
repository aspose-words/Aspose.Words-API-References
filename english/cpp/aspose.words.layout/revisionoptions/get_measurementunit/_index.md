---
title: Aspose::Words::Layout::RevisionOptions::get_MeasurementUnit method
linktitle: get_MeasurementUnit
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::RevisionOptions::get_MeasurementUnit method. Allows to specify the measurement units for revision comments. Default value is Centimeters in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.layout/revisionoptions/get_measurementunit/
---
## RevisionOptions::get_MeasurementUnit method


Allows to specify the measurement units for revision comments. Default value is [Centimeters](../../../aspose.words/measurementunits/)

```cpp
Aspose::Words::MeasurementUnits Aspose::Words::Layout::RevisionOptions::get_MeasurementUnit() const
```


## Examples



Shows how to make a saved document conform to an older ODT schema. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

## See Also

* Enum [MeasurementUnits](../../../aspose.words/measurementunits/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
