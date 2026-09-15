---
title: "فئة Aspose::Words::Border"
linktitle: "Border"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Border. تمثل حدًا لكائن. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/border/
---
## Border class


يمثل حدًا لكائن. لمعرفة المزيد، زر مقالة الوثائق [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Border : public Aspose::Words::InternableComplexAttr,
               public Aspose::Words::IComplexAttr
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | يعيد تعيين خصائص الحد إلى القيم الافتراضية. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Border\>\&) | يحدد ما إذا كان الحد المحدد مساويًا في القيمة للحد الحالي. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي. |
| [get_Color](./get_color/)() | يحصل أو يضبط لون الحد. |
| [get_DistanceFromText](./get_distancefromtext/)() | يحصل أو يضبط مسافة الحد من النص أو من حافة الصفحة بالنقاط. |
| [get_IsVisible](./get_isvisible/)() | يرجع **true** إذا كان [LineStyle](./get_linestyle/) ليس [None](../linestyle/). |
| [get_LineStyle](./get_linestyle/)() | يحصل أو يضبط نمط الحد. |
| [get_LineWidth](./get_linewidth/)() | يحصل أو يضبط عرض الحد بالنقاط. |
| [get_Shadow](./get_shadow/)() | يحصل أو يضبط قيمة تشير إلى ما إذا كان للحد ظل. |
| [get_ThemeColor](./get_themecolor/)() | يحصل أو يضبط لون السمة في مخطط الألوان المطبق المرتبط بهذا الكائن [Border](./). |
| [get_TintAndShade](./get_tintandshade/)() | يحصل أو يضبط قيمة مزدوجة تُفتح أو تُغمق اللون. |
| [GetHashCode](./gethashcode/)() const override | يعمل كدالة تجزئة لهذا النوع. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | دالة ضبط لـ [Aspose::Words::Border::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | دالة ضبط لـ [Aspose::Words::Border::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | دالة ضبط لـ [Aspose::Words::Border::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | دالة ضبط لـ [Aspose::Words::Border::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | دالة ضبط لـ [Aspose::Words::Border::get_Shadow](./get_shadow/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | دالة تعيين لـ [Aspose::Words::Border::get_ThemeColor](./get_themecolor/). |
| [set_TintAndShade](./set_tintandshade/)(double) | دالة تعيين لـ [Aspose::Words::Border::get_TintAndShade](./get_tintandshade/). |
| static [Type](./type/)() |  |
## ملاحظات


يمكن تطبيق الحدود على عناصر مستند مختلفة بما في ذلك الفقرة، ومجموعة النص داخل الفقرة أو خلية جدول.

## أمثلة



يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


يوضح كيفية إدراج فقرة ذات حد علوي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// قم بتعيين ThemeColor فقط عندما يتم تعيين LineWidth أو LineStyle.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## انظر أيضًا

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
