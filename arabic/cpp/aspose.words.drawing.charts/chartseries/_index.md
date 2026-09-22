---
title: "Aspose::Words::Drawing::Charts::ChartSeries class"
linktitle: "ChartSeries"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries class. تمثّل خصائص سلسلة المخطط. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class


يمثل خصائص سلسلة المخطط. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartSeries : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                    public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | يضيف قيمة X المحددة إلى سلسلة المخطط. إذا كانت السلسلة تدعم قيم Y وأحجام الفقاعات، فستكون فارغة بالنسبة لقيمة X. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | يضيف قيم X و Y المحددة إلى سلسلة المخطط. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | يضيف قيمة X المحددة، وقيمة Y، وحجم الفقاعة إلى سلسلة المخطط. |
| [Clear](./clear/)() | يزيل جميع قيم البيانات من سلسلة المخطط. يتم مسح تنسيق جميع نقاط البيانات الفردية وعناوين البيانات. |
| [ClearValues](./clearvalues/)() | يزيل جميع قيم البيانات من سلسلة المخطط مع الحفاظ على تنسيق نقاط البيانات وعناوين البيانات. |
| [CopyFormatFrom](./copyformatfrom/)(int32_t) | ينسخ تنسيق نقطة البيانات الافتراضي من نقطة البيانات ذات الفهرس المحدد. |
| [get_Bubble3D](./get_bubble3d/)() override | يحدد ما إذا كان يجب تطبيق تأثير ثلاثي الأبعاد على الفقاعات في مخطط الفقاعات. |
| [get_BubbleSizes](./get_bubblesizes/)() | يحصل على مجموعة أحجام الفقاعات لهذه السلسلة المخططة. |
| [get_DataLabels](./get_datalabels/)() | يحدد الإعدادات لعناوين البيانات للسلسلة بأكملها. |
| [get_DataPoints](./get_datapoints/)() const | يرجع مجموعة من كائنات التنسيق لجميع نقاط البيانات في هذه السلسلة. |
| [get_Explosion](./get_explosion/)() override | يحدد مقدار إزاحة نقطة البيانات من مركز الفطيرة. يمكن أن يكون سالبًا، السالب يعني أن الخاصية غير مضبوطة ولا يجب تطبيق أي انفجار. ينطبق فقط على مخططات الفطيرة. |
| [get_Format](./get_format/)() | يوفر الوصول إلى تنسيق التعبئة والخط للسلسلة. |
| [get_HasDataLabels](./get_hasdatalabels/)() const | يحصل أو يضبط علمًا يُشير إلى ما إذا كانت عناوين البيانات معروضة للسلسلة. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | يحدد ما إذا كان العنصر الأب سيعكس ألوانه إذا كانت القيمة سلبية. |
| [get_LegendEntry](./get_legendentry/)() | يحصل على مدخل في وسيلة الإيضاح لهذه السلسلة البيانية. |
| [get_Marker](./get_marker/)() override | يحدد علامة بيانات. يتم إنشاء العلامة تلقائيًا عند الطلب. |
| [get_Name](./get_name/)() | يحصل على اسم السلسلة، إذا لم يتم تعيين الاسم صراحةً يتم إنشاؤه باستخدام الفهرس. بشكل افتراضي يُرجع السلسلة مع فهرس يبدأ من واحد. |
| [get_SeriesType](./get_seriestype/)() | يحصل على نوع هذه السلسلة البيانية. |
| [get_Smooth](./get_smooth/)() const | يسمح بتحديد ما إذا كان الخط الذي يربط النقاط في المخطط يجب أن يُنعم باستخدام منحنيات Catmull‑Rom. |
| [get_XValues](./get_xvalues/)() | يحصل على مجموعة من قيم X لهذه السلسلة البيانية. |
| [get_YValues](./get_yvalues/)() | يحصل على مجموعة من قيم Y لهذه السلسلة البيانية. |
| [GetType](./gettype/)() const override |  |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | يدرج قيمة X المحددة في السلسلة البيانية عند الفهرس المحدد. إذا كانت السلسلة تدعم قيم Y وأحجام الفقاعات، فستكون فارغة بالنسبة لقيمة X. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | يدرج قيم X و Y المحددة في السلسلة البيانية عند الفهرس المحدد. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | يدرج قيمة X المحددة، وقيمة Y، وحجم الفقاعة في السلسلة البيانية عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | يزيل قيمة X وقيمة Y وحجم الفقاعة، إذا كان مدعومًا، من السلسلة البيانية عند الفهرس المحدد. كما يتم إزالة نقطة البيانات المقابلة وملصق البيانات. |
| [set_Bubble3D](./set_bubble3d/)(bool) override | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D](./get_bubble3d/). |
| [set_Explosion](./set_explosion/)(int32_t) override | يحدد مقدار إزاحة نقطة البيانات من مركز الفطيرة. يمكن أن يكون سالبًا، السالب يعني أن الخاصية غير مضبوطة ولا يجب تطبيق أي انفجار. ينطبق فقط على مخططات الفطيرة. |
| [set_HasDataLabels](./set_hasdatalabels/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels](./get_hasdatalabels/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | يحدد ما إذا كان العنصر الأب سيعكس ألوانه إذا كانت القيمة سلبية. |
| [set_Name](./set_name/)(const System::String\&) | يضبط اسم السلسلة، إذا لم يتم تعيين الاسم صراحةً يتم إنشاؤه باستخدام الفهرس. بشكل افتراضي يُرجع السلسلة مع فهرس يبدأ من واحد. |
| [set_Smooth](./set_smooth/)(bool) | يسمح بتحديد ما إذا كان الخط الذي يربط النقاط في المخطط يجب أن يُنعم باستخدام منحنيات Catmull‑Rom. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
