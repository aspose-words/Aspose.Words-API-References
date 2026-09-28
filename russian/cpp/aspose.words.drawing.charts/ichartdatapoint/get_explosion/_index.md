---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion метод"
linktitle: "get_Explosion"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion метод. Указывает величину, на которую точка данных должна быть смещена от центра круговой диаграммы. Может быть отрицательной; отрицательное значение означает, что свойство не задано и взрыв не должен применяться. Применяется только к круговым диаграммам в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.drawing.charts/ichartdatapoint/get_explosion/
---
## IChartDataPoint::get_Explosion method


Указывает величину, на которую точка данных должна быть смещена от центра круговой диаграммы. Может быть отрицательной; отрицательное значение означает, что свойство не установлено и взрыв не применяется. Применяется только к круговым диаграммам.

```cpp
virtual int32_t Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion()=0
```


## Примеры



Показывает, как переместить сегменты круговой диаграммы от центра.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Sales", chart->get_Series()->idx_get(0)->get_Name());

// "Slices" круговой диаграммы могут быть перемещены от центра на расстояние с помощью атрибута Explosion соответствующей точки данных.
// Добавьте точку данных в первый сегмент круговой диаграммы и переместите её от центра на 10 пунктов.
// Aspose.Words автоматически создает точки данных, если они не существуют.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(0);
dataPoint->set_Explosion(10);

// Сместите вторую часть на большее расстояние.
dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(1);
dataPoint->set_Explosion(40);

doc->Save(get_ArtifactsDir() + u"Charts.PieChartExplosion.docx");
```

## См. также

* Interface [IChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
