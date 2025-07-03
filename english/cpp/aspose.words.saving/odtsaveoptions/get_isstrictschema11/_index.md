---
title: Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 method
linktitle: get_IsStrictSchema11
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 method. Specifies whether export should correspond to ODT specification 1.1 strictly. OOo 3.0 displays files correctly when they contain elements and attributes of ODT 1.2. Use "false" for this purpose, or "true" for strict conformity of specification 1.1. The default value is false in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.saving/odtsaveoptions/get_isstrictschema11/
---
## OdtSaveOptions::get_IsStrictSchema11 method


Specifies whether export should correspond to ODT specification 1.1 strictly. OOo 3.0 displays files correctly when they contain elements and attributes of ODT 1.2. Use "false" for this purpose, or "true" for strict conformity of specification 1.1. The default value is **false**.

```cpp
bool Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11() const
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

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
