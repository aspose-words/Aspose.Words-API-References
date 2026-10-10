---
title: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 method"
linktitle: "get_IsStrictSchema11"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 yöntemi. Dışa aktarmanın ODT spesifikasyonu 1.1'e sıkı bir şekilde uyup uymadığını belirtir. OOo 3.0, dosyalar ODT 1.2'nin öğelerini ve özniteliklerini içerdiğinde dosyaları doğru gösterir. Bu amaçla \"false\" kullanın veya 1.1 spesifikasyonuna sıkı uyum için \"true\" kullanın. Varsayılan değer C++'ta false'tur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/odtsaveoptions/get_isstrictschema11/
---
## OdtSaveOptions::get_IsStrictSchema11 method


Dışa aktarımın ODT spesifikasyonu 1.1'e kesin olarak uyması gerekip gerekmediğini belirtir. OOo 3.0, ODT 1.2 öğeleri ve özniteliklerini içerdiğinde dosyaları doğru gösterir. Bu amaçla "false" kullanın veya spesifikasyon 1.1'e sıkı uyum için "true" kullanın. Varsayılan değer **false** dir.

```cpp
bool Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11() const
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

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
