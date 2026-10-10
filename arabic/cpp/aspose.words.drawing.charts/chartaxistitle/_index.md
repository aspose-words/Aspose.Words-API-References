---
title: "Aspose::Words::Drawing::Charts::ChartAxisTitle class"
linktitle: "ChartAxisTitle"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartAxisTitle class. يوفّر الوصول إلى خصائص عنوان المحور. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 5750
url: /ar/cpp/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class


يوفر الوصول إلى خصائص عنوان المحور. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartAxisTitle : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Font](./get_font/)() | يوفر الوصول إلى تنسيق الخط لعنوان المحور. |
| [get_Format](./get_format/)() | يوفر الوصول إلى تنسيق التعبئة والخط لعنوان المحور. |
| [get_Orientation](./get_orientation/)() | يسترجع أو يعيّن اتجاه نص عنوان المحور. |
| [get_Overlay](./get_overlay/)() | يحدد ما إذا كان يُسمح لعناصر المخطط الأخرى بتغطية العنوان. القيمة الافتراضية هي **false**. |
| [get_Rotation](./get_rotation/)() | يسترجع أو يعيّن دوران عنوان المحور بالدرجات. |
| [get_Show](./get_show/)() | يحدد ما إذا كان يجب عرض العنوان للمحور. القيمة الافتراضية هي **false**. |
| [get_Text](./get_text/)() | يسترجع أو يعيّن نص عنوان المحور. إذا تم تحديد **null** أو قيمة فارغة، سيظهر عنوان مُولَّد تلقائيًا. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | محدد لـ [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Orientation](./get_orientation/). |
| [set_Overlay](./set_overlay/)(bool) | محدد لـ [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Overlay](./get_overlay/). |
| [set_Rotation](./set_rotation/)(int32_t) | محدد لـ [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation](./get_rotation/). |
| [set_Show](./set_show/)(bool) | محدد لـ [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | محدد لـ [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text](./get_text/). |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية تعيين عنوان محور المخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// حذف السلسلة التي تم إنشاؤها افتراضيًا.
seriesColl->Clear();

seriesColl->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2"}), System::MakeArray<double>({1, 2}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisXTitle = chart->get_AxisX()->get_Title();
chartAxisXTitle->set_Text(u"Categories");
chartAxisXTitle->set_Show(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisYTitle = chart->get_AxisY()->get_Title();
chartAxisYTitle->set_Text(u"Values");
chartAxisYTitle->set_Show(true);
chartAxisYTitle->set_Overlay(true);
chartAxisYTitle->get_Font()->set_Size(12);
chartAxisYTitle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.ChartAxisTitle.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
