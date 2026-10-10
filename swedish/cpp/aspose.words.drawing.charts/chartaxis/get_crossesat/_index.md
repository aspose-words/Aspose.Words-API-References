---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt metod"
linktitle: "get_CrossesAt"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt metod. Anger var på den vinkelräta axeln som axeln korsar i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.drawing.charts/chartaxis/get_crossesat/
---
## ChartAxis::get_CrossesAt method


Anger var på den vinkelräta axeln axeln korsar.

```cpp
double Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt()
```

## Anmärkningar


Egenskapen har effekt endast om [Crosses](../get_crosses/) är inställd på [Custom](../../axiscrosses/). Den stöds inte av de nya diagrammen i MS Office 2016.

Enheterna bestäms av axeltypen. När axeln är en värdeaxel är egenskapens värde ett decimaltal på värdeaxeln. När axeln är en tidskategorisk axel definieras värdet som ett heltal antal dagar relativt till basdatumet (30/12/1899). För en textkategorisk axel är värdet ett heltal kategori‑nummer, med 1 som den första kategorin.

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
