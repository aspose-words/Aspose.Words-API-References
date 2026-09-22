---
title: "فئة Aspose::Words::Drawing::Charts::ChartAxis"
linktitle: "ChartAxis"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Drawing::Charts::ChartAxis. تمثل خيارات المحور للمخطط. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class


يمثل خيارات المحور للمخطط. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartAxis : public Aspose::Words::Drawing::Charts::Core::IDmlChartTitleHolder,
                  public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                  public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                  public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_AxisBetweenCategories](./get_axisbetweencategories/)() | يحصل أو يعيّن علمًا يشير إلى ما إذا كان محور القيمة يعبر محور الفئة بين الفئات. |
| [get_BaseTimeUnit](./get_basetimeunit/)() | يرجع أو يعيّن أصغر وحدة زمنية يتم تمثيلها على محور الفئة الزمنية. |
| [get_CategoryType](./get_categorytype/)() | يحصل أو يعيّن نوع محور الفئة. |
| [get_Crosses](./get_crosses/)() | يحدد كيف يعبر هذا المحور المحور العمودي. |
| [get_CrossesAt](./get_crossesat/)() | يحدد أين على المحور العمودي يعبر المحور. |
| [get_DisplayUnit](./get_displayunit/)() | يحدد قيمة التحجيم لوحدات العرض لمحور القيمة. |
| [get_Document](./get_document/)() | يرجع المستند الذي يحتوي على المخطط الأب. |
| [get_Format](./get_format/)() | يوفر الوصول إلى تنسيق الخط للمحور وتعبئة تسميات العلامات. |
| [get_HasMajorGridlines](./get_hasmajorgridlines/)() | يحصل أو يعيّن علمًا يشير إلى ما إذا كان للمحور خطوط شبكة رئيسية. |
| [get_HasMinorGridlines](./get_hasminorgridlines/)() | يحصل أو يعيّن علمًا يشير إلى ما إذا كان للمحور خطوط شبكة فرعية. |
| [get_Hidden](./get_hidden/)() | يحصل أو يعيّن علمًا يشير إلى ما إذا كان هذا المحور مخفيًا أم لا. |
| [get_MajorTickMark](./get_majortickmark/)() | يرجع أو يعيّن العلامات الرئيسية. |
| [get_MajorUnit](./get_majorunit/)() | يرجع أو يعيّن المسافة بين العلامات الرئيسية. |
| [get_MajorUnitIsAuto](./get_majorunitisauto/)() | يحصل أو يعيّن علمًا يشير إلى ما إذا كان يجب استخدام المسافة الافتراضية بين العلامات الرئيسية. |
| [get_MajorUnitScale](./get_majorunitscale/)() | يرجع أو يعيّن قيمة المقياس للعلامات الرئيسية على محور الفئة الزمنية. |
| [get_MinorTickMark](./get_minortickmark/)() | يرجع أو يعيّن العلامات الفرعية للمحور. |
| [get_MinorUnit](./get_minorunit/)() | يرجع أو يعيّن المسافة بين العلامات الفرعية. |
| [get_MinorUnitIsAuto](./get_minorunitisauto/)() | يحصل أو يعيّن علمًا يشير إلى ما إذا كان يجب استخدام المسافة الافتراضية بين العلامات الفرعية. |
| [get_MinorUnitScale](./get_minorunitscale/)() | يرجع أو يعيّن قيمة المقياس للعلامات الفرعية على محور الفئة الزمنية. |
| [get_NumberFormat](./get_numberformat/)() | يرجع كائنًا من نوع [ChartNumberFormat](../chartnumberformat/) يسمح بتعريف تنسيقات الأرقام للمحور. |
| [get_ReverseOrder](./get_reverseorder/)() | يرجع أو يعيّن علمًا يشير إلى ما إذا كان يجب عرض قيم المحور بترتيب عكسي، أي من الحد الأقصى إلى الحد الأدنى. |
| [get_Scaling](./get_scaling/)() | يوفر الوصول إلى خيارات التحجيم للمحور. |
| [get_TickLabels](./get_ticklabels/)() | يوفر الوصول إلى خصائص تسميات علامات الفواصل للمحور. |
| [get_TickMarkSpacing](./get_tickmarkspacing/)() | يحصل أو يضبط الفاصل الذي تُرسم عنده علامات الفواصل. |
| [get_Title](./get_title/)() | يوفر الوصول إلى خصائص عنوان المحور. |
| [get_Type](./get_type/)() const | يرجع نوع المحور. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisBetweenCategories](./set_axisbetweencategories/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories](./get_axisbetweencategories/). |
| [set_BaseTimeUnit](./set_basetimeunit/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_BaseTimeUnit](./get_basetimeunit/). |
| [set_CategoryType](./set_categorytype/)(Aspose::Words::Drawing::Charts::AxisCategoryType) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_CategoryType](./get_categorytype/). |
| [set_Crosses](./set_crosses/)(Aspose::Words::Drawing::Charts::AxisCrosses) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_Crosses](./get_crosses/). |
| [set_CrossesAt](./set_crossesat/)(double) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt](./get_crossesat/). |
| [set_HasMajorGridlines](./set_hasmajorgridlines/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMajorGridlines](./get_hasmajorgridlines/). |
| [set_HasMinorGridlines](./set_hasminorgridlines/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMinorGridlines](./get_hasminorgridlines/). |
| [set_Hidden](./set_hidden/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden](./get_hidden/). |
| [set_MajorTickMark](./set_majortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorTickMark](./get_majortickmark/). |
| [set_MajorUnit](./set_majorunit/)(double) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnit](./get_majorunit/). |
| [set_MajorUnitIsAuto](./set_majorunitisauto/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitIsAuto](./get_majorunitisauto/). |
| [set_MajorUnitScale](./set_majorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitScale](./get_majorunitscale/). |
| [set_MinorTickMark](./set_minortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorTickMark](./get_minortickmark/). |
| [set_MinorUnit](./set_minorunit/)(double) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnit](./get_minorunit/). |
| [set_MinorUnitIsAuto](./set_minorunitisauto/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitIsAuto](./get_minorunitisauto/). |
| [set_MinorUnitScale](./set_minorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale](./get_minorunitscale/). |
| [set_ReverseOrder](./set_reverseorder/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_ReverseOrder](./get_reverseorder/). |
| [set_TickMarkSpacing](./set_tickmarkspacing/)(int32_t) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartAxis::get_TickMarkSpacing](./get_tickmarkspacing/). |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية إدراج مخطط وتعديل مظهر محاوره.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// امسح سلسلة بيانات العرض التجريبية للمخطط للبدء بمخطط نظيف.
chart->get_Series()->Clear();

// أدرج سلسلة مخطط مع فئات لمحور X والقيم الرقمية المقابلة لمحور Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({640, 320, 280, 120, 150}));

// للمحاور في المخطط خيارات متعددة يمكنها تغيير مظهرها،
// مثل اتجاهها، علامات الوحدات الرئيسية/الصغرى، وعلامات الفواصل.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Category);
xAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Minimum);
xAxis->set_ReverseOrder(false);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MajorUnit(10.0);
xAxis->set_MinorUnit(15.0);
xAxis->get_TickLabels()->set_Offset(50);
xAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::Low);
xAxis->get_TickLabels()->set_IsAutoSpacing(false);
xAxis->set_TickMarkSpacing(1);

ASPOSE_ASSERT_EQ(doc, xAxis->get_Document());

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Automatic);
yAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Maximum);
yAxis->set_ReverseOrder(true);
yAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
yAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(20.0);
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::NextToAxis);
yAxis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
yAxis->get_TickLabels()->get_Font()->set_Color(System::Drawing::Color::get_Red());
yAxis->get_TickLabels()->set_Spacing(1);

// المخططات العمودية لا تحتوي على محور Z.
ASSERT_TRUE(System::TestTools::IsNull(chart->get_AxisZ()));

doc->Save(get_ArtifactsDir() + u"Charts.AxisProperties.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
