---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize метод"
linktitle: "get_ShowBubbleSize"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize метод. Позволяет указать, следует ли отображать размер пузыря в метках данных на диаграмме. Применяется только к пузырьковым диаграммам. Значение по умолчанию — false в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.drawing.charts/chartdatalabel/get_showbubblesize/
---
## ChartDataLabel::get_ShowBubbleSize method


Позволяет указать, следует ли отображать размер пузыря для подписей данных на диаграмме. Применяется только к пузырьковым диаграммам. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize()
```


## Примеры



Показывает, как использовать 3D‑эффекты с пузырьковыми диаграммами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_TRUE(chart->get_Series()->idx_get(0)->get_Bubble3D());

// Примените подпись данных к каждому пузырьку, отображающую его диаметр.
for (int32_t i = 0; i < 3; i++)
{
    chart->get_Series()->idx_get(0)->set_HasDataLabels(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->set_ShowBubbleSize(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->get_Font()->set_Size(12);
}

doc->Save(get_ArtifactsDir() + u"Charts.Bubble3D.docx");
```

## См. также

* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
