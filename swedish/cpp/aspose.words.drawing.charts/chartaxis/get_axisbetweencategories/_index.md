---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories metod"
linktitle: "get_AxisBetweenCategories"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories metod. Hämtar eller anger en flagga som indikerar om värdeaxeln korsar kategoriaxeln mellan kategorier i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.drawing.charts/chartaxis/get_axisbetweencategories/
---
## ChartAxis::get_AxisBetweenCategories method


Hämtar eller anger en flagga som indikerar om värdeaxeln korsar kategoriaxeln mellan kategorier.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories()
```


## Exempel



Visar hur man får en diagramaxel att korsas på en anpassad plats.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// För stapeldiagram korsar Y‑axeln noll som standard,
// vilket betyder att staplar för alla värden under noll pekar nedåt för att representera negativa värden.
// Vi kan ange ett annat värde för Y‑axelns korsning. I det här fallet sätter vi den till 3.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisX();
axis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Custom);
axis->set_CrossesAt(3);
axis->set_AxisBetweenCategories(true);

doc->Save(get_ArtifactsDir() + u"Charts.AxisCross.docx");
```

## Se även

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
