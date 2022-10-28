---
title: get_AxisBetweenCategories
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a flag indicating whether the value axis crosses the category axis between categories.
type: docs
weight: 1
url: /cpp/aspose.words.drawing.charts/chartaxis/get_axisbetweencategories/
---
## ChartAxis.get_AxisBetweenCategories method


Gets or sets a flag indicating whether the value axis crosses the category axis between categories.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories()
```


## Examples




Shows how to get a graph axis to cross at a custom location. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertChart(ChartType::Column, 450, 250);
SharedPtr<Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// For column charts, the Y-axis crosses at zero by default,
// which means that columns for all values below zero point down to represent negative values.
// We can set a different value for the Y-axis crossing. In this case, we will set it to 3.
SharedPtr<ChartAxis> axis = chart->get_AxisX();
axis->set_Crosses(AxisCrosses::Custom);
axis->set_CrossesAt(3);
axis->set_AxisBetweenCategories(true);

doc->Save(ArtifactsDir + u"Charts.AxisCross.docx");
```

