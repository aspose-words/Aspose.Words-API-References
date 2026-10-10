---
title: "Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit yöntemi"
linktitle: "get_MeasureUnit"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit yöntemi. Belge içeriğine uygulanacak ölçü birimlerini belirtmeye izin verir. Varsayılan değer C++'ta Centimeters'tir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/odtsaveoptions/get_measureunit/
---
## OdtSaveOptions::get_MeasureUnit method


Belge içeriğine uygulanacak ölçü birimlerini belirtmeye izin verir. Varsayılan değer [Centimeters](../../odtsavemeasureunit/)

```cpp
Aspose::Words::Saving::OdtSaveMeasureUnit Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit() const
```


## Örnekler



Kaydedilmiş bir belgenin eski bir ODT şemasına uygun hale getirilmesini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Ayrıca Bakınız

* Enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
