---
title: "Aspose::Words::Drawing::ShapeTextOrientation enum"
linktitle: "ShapeTextOrientation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeTextOrientation enum. يحدد اتجاه النص داخل الأشكال في C++."
type: docs
weight: 37500
url: /ar/cpp/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enum


يحدد اتجاه النص في الأشكال.

```cpp
enum class ShapeTextOrientation
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| أفقي | 0 | النص مُرتب أفقيًا (lr-tb). |
| أسفل | 1 | النص مُدوَّر 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل (tb-rl). |
| أعلى | 2 | النص مُدوَّر 90 درجة إلى اليسار ليظهر من الأسفل إلى الأعلى (bt-lr). |
| VerticalFarEast | 3 | تظهر أحرف الشرق الأقصى عموديًا، والنص الآخر يُدوَّر 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل (tb-rl-v). |
| VerticalRotatedFarEast | 4 | تظهر أحرف الشرق الأقصى عموديًا، والنص الآخر يُدوَّر 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل عموديًا، ثم من اليسار إلى اليمين أفقيًا (tb-lr-v). |
| WordArtVertical | 5 | النص عمودي، بحرف واحد فوق الآخر. |
| WordArtVerticalRightToLeft | 6 | النص عمودي، بحرف واحد فوق الآخر، ثم من اليمين إلى اليسار أفقياً. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
