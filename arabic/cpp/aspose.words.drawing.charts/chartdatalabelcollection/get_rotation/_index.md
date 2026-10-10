---
title: "طريقة Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation"
linktitle: "get_Rotation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation. يحصل على أو يعيّن دوران تسميات البيانات للسلسلة بأكملها بالدرجات في C++."
type: docs
weight: 5667
url: /ar/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_rotation/
---
## ChartDataLabelCollection::get_Rotation method


يحصل أو يضبط دوران تسميات البيانات للسلسلة بأكملها بالدرجات.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation()
```

## ملاحظات


نطاق القيم المقبولة هو من -180 إلى 180 شاملًا. القيمة الافتراضية هي 0.

إذا كانت قيمة [Orientation](../get_orientation/) هي [Horizontal](../../../aspose.words.drawing/shapetextorientation/)، تُدوَّر أشكال التسمية، إن وجدت، مع نص التسمية. وإلا، يُدوَّر نص التسمية فقط.

## أمثلة



يوضح كيفية تغيير الاتجاه والدوران لتسميات البيانات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();

// إظهار تسميات البيانات.
series->set_HasDataLabels(true);
dataLabels->set_ShowValue(true);
dataLabels->set_ShowCategoryName(true);

// تحديد شكل تسمية البيانات.
dataLabels->get_Format()->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::UpArrow);
dataLabels->get_Format()->get_Stroke()->get_Fill()->Solid(System::Drawing::Color::get_DarkBlue());

// تعيين اتجاه وتدوير تسمية البيانات للسلسلة بأكملها.
dataLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
dataLabels->set_Rotation(-45);

// تغيير اتجاه وتدوير أول تسمية بيانات.
dataLabels->idx_get(0)->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
dataLabels->idx_get(0)->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.LabelOrientationRotation.docx");
```

## انظر أيضًا

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
