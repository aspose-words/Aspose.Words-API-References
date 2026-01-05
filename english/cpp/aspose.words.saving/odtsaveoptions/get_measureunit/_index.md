---
title: Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit method
linktitle: get_MeasureUnit
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit method. Allows to specify units of measure to apply to document content. The default value is Centimeters in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.saving/odtsaveoptions/get_measureunit/
---
## OdtSaveOptions::get_MeasureUnit method


Allows to specify units of measure to apply to document content. The default value is [Centimeters](../../odtsavemeasureunit/)

```cpp
Aspose::Words::Saving::OdtSaveMeasureUnit Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit() const
```


## Examples



Shows how to make a saved document conform to an older ODT schema. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## See Also

* Enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
