---
title: "Aspose::Words::Drawing::Charts::ChartLegend class"
linktitle: "ChartLegend"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartLegend class. يمثل خصائص وسيلة إيضاح المخطط. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class


يمثل خصائص وسيلة إيضاح المخطط. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartLegend : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                    public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Font](./get_font/)() | يوفر الوصول إلى تنسيق الخط الافتراضي لمدخلات وسيلة الإيضاح. لتجاوز تنسيق الخط لمدخل وسيلة إيضاح محدد، استخدم خاصية [Font](../chartlegendentry/get_font/). |
| [get_Format](./get_format/)() | يوفر الوصول إلى تنسيق التعبئة والخط لوسيلة الإيضاح. |
| [get_LegendEntries](./get_legendentries/)() const | يرجع مجموعة من مدخلات وسيلة الإيضاح لجميع السلاسل وخطوط الاتجاه للمخطط الأصلي. |
| [get_Overlay](./get_overlay/)() const | يحدد ما إذا كان يُسمح لعناصر المخطط الأخرى بالتداخل مع وسيلة الإيضاح. القيمة الافتراضية هي **false**. |
| [get_Position](./get_position/)() | يحدد موضع وسيلة الإيضاح على المخطط. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Overlay](./set_overlay/)(bool) | محدد لـ [Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay](./get_overlay/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::LegendPosition) | محدد لـ [Aspose::Words::Drawing::Charts::ChartLegend::get_Position](./get_position/). |
| static [Type](./type/)() |  |

## أمثلة



يظهر كيفية تعديل مظهر وسيلة إيضاح المخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// انقل وسيلة إيضاح المخطط إلى الزاوية العليا اليمنى.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// امنح عناصر المخطط الأخرى، مثل الرسم البياني، مساحة أكبر بالسماح لها بالتداخل مع وسيلة الإيضاح.
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
