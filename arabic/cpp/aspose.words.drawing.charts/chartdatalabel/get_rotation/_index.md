---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation طريقة"
linktitle: "get_Rotation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation طريقة. يحصل أو يضبط دوران التسمية بالدرجات في C++."
type: docs
weight: 7667
url: /ar/cpp/aspose.words.drawing.charts/chartdatalabel/get_rotation/
---
## ChartDataLabel::get_Rotation method


يحصل أو يضبط دوران التسمية بالدرجات.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation()
```

## ملاحظات


نطاق القيم المقبولة هو من -180 إلى 180 شاملًا. القيمة الافتراضية هي 0.

إذا كانت قيمة [الاتجاه](../get_orientation/) هي [أفقي](../../../aspose.words.drawing/shapetextorientation/)، فإن شكل التسمية، إذا كان موجودًا، يتم تدويره مع نص التسمية. وإلا، يتم تدوير نص التسمية فقط.

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

* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
