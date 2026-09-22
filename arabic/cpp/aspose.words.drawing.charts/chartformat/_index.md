---
title: "Aspose::Words::Drawing::Charts::ChartFormat class"
linktitle: "ChartFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartFormat class. يمثل تنسيق عنصر المخطط. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class


يمثل تنسيق عنصر المخطط. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartFormat : public Aspose::Words::Drawing::Core::IFillable,
                    public Aspose::Words::Drawing::Core::IStrokable
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Fill](./get_fill/)() | يحصل على تنسيق التعبئة لعنصر المخطط الأب. |
| [get_IsDefined](./get_isdefined/)() | يحصل على علم يشير إلى ما إذا كان هناك أي تنسيق معرف. |
| [get_ShapeType](./get_shapetype/)() | يحصل أو يضبط نوع الشكل لعنصر المخطط الأب. |
| [get_Stroke](./get_stroke/)() | يحصل على تنسيق الخط لعنصر المخطط الأب. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ShapeType](./set_shapetype/)(Aspose::Words::Drawing::Charts::ChartShapeType) | المُعيّن لـ [Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType](./get_shapetype/). |
| [SetDefaultFill](./setdefaultfill/)() | يعيد تعيين تعبئة عنصر المخطط إلى القيمة الافتراضية. |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية استخدام تنسيق المخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// حذف السلاسل التي تم إنشاؤها افتراضيًا.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});
series->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
series->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));

// تنسيق خلفية المخطط.
chart->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_DarkSlateGray());

// إخفاء تسميات علامات المحور.
chart->get_AxisX()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);
chart->get_AxisY()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);

// تنسيق عنوان المخطط.
chart->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// تنسيق عنوان المحور.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// تنسيق المفتاح.
chart->get_Legend()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

doc->Save(get_ArtifactsDir() + u"Charts.ChartFormat.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
