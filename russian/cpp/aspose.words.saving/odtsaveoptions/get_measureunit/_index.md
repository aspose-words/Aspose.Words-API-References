---
title: "Метод Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit"
linktitle: "get_MeasureUnit"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit. Позволяет задавать единицы измерения, применяемые к содержимому документа. Значение по умолчанию — Centimeters в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/odtsaveoptions/get_measureunit/
---
## OdtSaveOptions::get_MeasureUnit method


Позволяет задавать единицы измерения, применяемые к содержимому документа. Значение по умолчанию — [Centimeters](../../odtsavemeasureunit/)

```cpp
Aspose::Words::Saving::OdtSaveMeasureUnit Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit() const
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

* Enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
