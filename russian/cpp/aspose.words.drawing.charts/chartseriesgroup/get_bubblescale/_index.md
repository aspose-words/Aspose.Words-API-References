---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale метод"
linktitle: "get_BubbleScale"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale метод. Получает или задает размер пузырей в процентах от их размера по умолчанию в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.drawing.charts/chartseriesgroup/get_bubblescale/
---
## ChartSeriesGroup::get_BubbleScale method


Получает или задает размер пузырей в процентах от их размера по умолчанию.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale()
```

## Примечания


Применяется только к группам рядов типов [Bubble](../../chartseriestype/) и [Bubble3D](../../chartseriestype/).

Диапазон допустимых значений от 0 до 300 включительно. Значение по умолчанию — 100.

## Примеры



Показать, как задать размер пузырей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставить 3D‑диаграмму пузырей.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Установить масштаб пузырей на 200%.
seriesGroup->set_BubbleScale(200);

doc->Save(get_ArtifactsDir() + u"Charts.BubbleScale.docx");
```

## См. также

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
