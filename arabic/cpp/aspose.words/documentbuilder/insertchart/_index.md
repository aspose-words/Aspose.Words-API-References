---
title: "Aspose::Words::DocumentBuilder::InsertChart طريقة"
linktitle: "InsertChart"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::InsertChart. تُدرج كائن مخطط في المستند وتقوم بتغيير حجمه إلى الحجم المحدد في C++."
type: docs
weight: 30000
url: /ar/cpp/aspose.words/documentbuilder/insertchart/
---
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


يدرج كائن مخطط في المستند ويقيسه إلى الحجم المحدد.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | نوع المخطط الذي سيتم إدراجه في المستند. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | يحدد من أين يُقاس المسافة إلى الصورة. |
| left | double | المسافة بالنقاط من الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | يحدد من أين تُقاس المسافة إلى الصورة. |
| top | double | المسافة بالنقاط من الأصل إلى الجانب العلوي من الصورة. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| wrapType | Aspose::Words::Drawing::WrapType | يحدد كيفية لف النص حول الصورة. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

## أمثلة



يوضح كيفية تحديد الموضع والتفاف النص أثناء إدراج مخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100, 200, 100, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertedChartRelativePosition.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) method


يدرج كائن مخطط في المستند ويقيسه إلى الحجم المحدد.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | نوع المخطط الذي سيتم إدراجه في المستند. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | يحدد من أين يُقاس المسافة إلى الصورة. |
| left | double | المسافة بالنقاط من الأصل إلى الجانب الأيسر من الصورة. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | يحدد من أين تُقاس المسافة إلى الصورة. |
| top | double | المسافة بالنقاط من الأصل إلى الجانب العلوي من الصورة. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| wrapType | Aspose::Words::Drawing::WrapType | يحدد كيفية لف النص حول الصورة. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | نمط المخطط المُدرج. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double) method


يدرج كائن مخطط في المستند ويقيسه إلى الحجم المحدد.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | نوع المخطط الذي سيتم إدراجه في المستند. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

## أمثلة



يوضح كيفية إدراج مخطط دائري في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::ConvertUtil::PixelToPoint(300), Aspose::Words::ConvertUtil::PixelToPoint(300))->get_Chart();
chart->get_Series()->Clear();
chart->get_Series()->Add(u"My fruit", System::MakeArray<System::String>({u"Apples", u"Bananas", u"Cherries"}), System::MakeArray<double>({1.3, 2.2, 1.5}));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertPieChart.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) method


يدرج كائن مخطط في المستند ويقيسه إلى الحجم المحدد.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | نوع المخطط الذي سيتم إدراجه في المستند. |
| العرض | double | عرض الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| الارتفاع | double | ارتفاع الصورة بالنقاط. يمكن أن يكون قيمة سالبة أو صفر لطلب مقياس 100٪. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | نمط المخطط المُدرج. |

### ReturnValue

عقدة الصورة التي تم إدراجها للتو.
## ملاحظات


يمكنك تغيير حجم الصورة، موقعها، طريقة تموضعها وإعدادات أخرى باستخدام كائن [Shape](../../../aspose.words.drawing/shape/) الذي تُعيده هذه الطريقة.

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
