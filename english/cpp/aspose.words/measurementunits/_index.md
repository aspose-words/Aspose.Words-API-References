---
title: Aspose::Words::MeasurementUnits enum
linktitle: MeasurementUnits
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MeasurementUnits enum. Specifies the unit of measurement in C++.'
type: docs
weight: 100000
url: /cpp/aspose.words/measurementunits/
---
## MeasurementUnits enum


Specifies the unit of measurement.

```cpp
enum class MeasurementUnits
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Inches | 0 | Inches. |
| Centimeters | 1 | Centimeters. |
| Millimeters | 2 | Millimeters. |
| Points | 3 | Points. |
| Picas | 4 | Picas (commonly used in traditional typewriter font spacing). |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
