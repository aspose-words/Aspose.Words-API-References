---
title: get_MeasureUnit
second_title: Aspose.Words for C++ API Reference
description: Allows to specify units of measure to apply to document content. The default value is Centimeters
type: docs
weight: 40
url: /cpp/aspose.words.saving/odtsaveoptions/get_measureunit/
---
## OdtSaveOptions::get_MeasureUnit method


Allows to specify units of measure to apply to document content. The default value is [Centimeters](../../odtsavemeasureunit/)

```cpp
Aspose::Words::Saving::OdtSaveMeasureUnit Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit() const
```


## Examples



Shows how to use different measurement units to define style parameters of a saved ODT document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// When we export the document to .odt, we can use an OdtSaveOptions object to modify how we save the document.
// We can set the "MeasureUnit" property to "OdtSaveMeasureUnit.Centimeters"
// to define content such as style parameters using the metric system, which Open Office uses.
// We can set the "MeasureUnit" property to "OdtSaveMeasureUnit.Inches"
// to define content such as style parameters using the imperial system, which Microsoft Word uses.
auto saveOptions = MakeObject<OdtSaveOptions>();
saveOptions->set_MeasureUnit(odtSaveMeasureUnit);

doc->Save(ArtifactsDir + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

## See Also

* Enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
