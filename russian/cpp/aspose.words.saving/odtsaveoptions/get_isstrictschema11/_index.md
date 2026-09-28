---
title: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 method"
linktitle: "get_IsStrictSchema11"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11. Указывает, должна ли экспорт соответствовать спецификации ODT 1.1 строго. OOo 3.0 корректно отображает файлы, когда они содержат элементы и атрибуты ODT 1.2. Используйте \"false\" для этой цели или \"true\" для строгого соответствия спецификации 1.1. Значение по умолчанию — false в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.saving/odtsaveoptions/get_isstrictschema11/
---
## OdtSaveOptions::get_IsStrictSchema11 method


Указывает, следует ли экспортировать строго в соответствии со спецификацией ODT 1.1. OOo 3.0 корректно отображает файлы, когда они содержат элементы и атрибуты ODT 1.2. Используйте "false" для этой цели или "true" для строгого соответствия спецификации 1.1. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11() const
```


## Примеры



Показывает, как сделать сохранённый документ соответствующим более старой схеме ODT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## См. также

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
