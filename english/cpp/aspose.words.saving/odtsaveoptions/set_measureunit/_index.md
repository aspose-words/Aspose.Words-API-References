---
title: Aspose::Words::Saving::OdtSaveOptions::set_MeasureUnit method
linktitle: set_MeasureUnit
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::OdtSaveOptions::set_MeasureUnit method. Allows to specify units of measure to apply to document content. The default value is Centimeters in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.saving/odtsaveoptions/set_measureunit/
---
## OdtSaveOptions::set_MeasureUnit method


Allows to specify units of measure to apply to document content. The default value is [Centimeters](../../odtsavemeasureunit/)

```cpp
void Aspose::Words::Saving::OdtSaveOptions::set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit value)
```

## Remarks

 Open Office uses centimeters when specifying lengths, widths and other measurable formatting and content properties in documents whereas MS Office uses inches. 
## Examples


Shows how to make a saved document conform to an older ODT schema.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rendering.docx"));

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt"));
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```
## See Also

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
