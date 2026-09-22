---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt طريقة"
linktitle: "get_CrossesAt"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt. تحدد المكان الذي يتقاطع فيه المحور على المحور العمودي في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.drawing.charts/chartaxis/get_crossesat/
---
## ChartAxis::get_CrossesAt method


يحدد أين على المحور العمودي يعبر المحور.

```cpp
double Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt()
```

## ملاحظات


الخاصية لها تأثير فقط إذا تم تعيين [Crosses](../get_crosses/) إلى [Custom](../../axiscrosses/). لا يتم دعمها في المخططات الجديدة لـ MS Office 2016.

الوحدات تُحدد بنوع المحور. عندما يكون المحور محور قيمة، تكون قيمة الخاصية رقمًا عشريًا على محور القيمة. عندما يكون المحور محور فئة زمنية، تُعرف القيمة كعدد صحيح من الأيام بالنسبة إلى التاريخ الأساسي (30/12/1899). بالنسبة لمحور فئة نصية، تكون القيمة رقم فئة صحيح، يبدأ بـ 1 كالفئة الأولى.

## أمثلة



يوضح كيفية جعل محور الرسم يتقاطع عند موقع مخصص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// في المخططات العمودية، يعبر المحور Y الصفر افتراضيًا،
// مما يعني أن الأعمدة لجميع القيم التي تقل عن الصفر تتجه للأسفل لتمثيل القيم السالبة.
// يمكننا تعيين قيمة مختلفة لتقاطع المحور Y. في هذه الحالة، سنضبطه على 3.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisX();
axis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Custom);
axis->set_CrossesAt(3);
axis->set_AxisBetweenCategories(true);

doc->Save(get_ArtifactsDir() + u"Charts.AxisCross.docx");
```

## انظر أيضًا

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
