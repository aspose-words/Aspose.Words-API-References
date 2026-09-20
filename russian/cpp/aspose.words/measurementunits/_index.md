---
title: "Aspose::Words::MeasurementUnits enum"
linktitle: "MeasurementUnits"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::MeasurementUnits enum. Указывает единицу измерения в C++."
type: docs
weight: 100000
url: /ru/cpp/aspose.words/measurementunits/
---
## MeasurementUnits enum


Указывает единицу измерения.

```cpp
enum class MeasurementUnits
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Дюймы | 0 | Дюймы. |
| Сантиметры | 1 | Сантиметры. |
| Миллиметры | 2 | Миллиметры. |
| Пункты | 3 | Пункты. |
| Пики | 4 | Пики (обычно используются в традиционном межсимвольном интервале машинописных шрифтов). |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
