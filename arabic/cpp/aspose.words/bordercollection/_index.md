---
title: "فئة Aspose::Words::BorderCollection"
linktitle: "BorderCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::BorderCollection. مجموعة من كائنات Border. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words/bordercollection/
---
## BorderCollection class


مجموعة من كائنات [Border](../border/) . لمعرفة المزيد، زر مقالة الوثائق [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class BorderCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Border>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | يزيل جميع حدود الكائن. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::BorderCollection\>\&) | يقارن مجموعات الحدود. |
| [get_Bottom](./get_bottom/)() | يحصل على الحد السفلي. |
| [get_Color](./get_color/)() | يحصل أو يضبط لون الحد. |
| [get_Count](./get_count/)() | يحصل على عدد الحدود في المجموعة. |
| [get_DistanceFromText](./get_distancefromtext/)() | يحصل أو يضبط المسافة بين الحد والنص بالنقاط. |
| [get_Horizontal](./get_horizontal/)() | يحصل على الحد الأفقي المستخدم بين الخلايا أو الفقرات المتوافقة. |
| [get_Left](./get_left/)() | يحصل على الحد الأيسر. |
| [get_LineStyle](./get_linestyle/)() | يحصل أو يضبط نمط الحد. |
| [get_LineWidth](./get_linewidth/)() | يحصل أو يضبط عرض الحد بالنقاط. |
| [get_Right](./get_right/)() | يحصل على الحد الأيمن. |
| [get_Shadow](./get_shadow/)() | يحصل أو يضبط قيمة تشير إلى ما إذا كان للحد ظل. |
| [get_Top](./get_top/)() | يحصل على الحد العلوي. |
| [get_Vertical](./get_vertical/)() | يحصل على الحد العمودي المستخدم بين الخلايا. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عداد يمكن استخدامه للتنقل عبر جميع الحدود في المجموعة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::BorderType) | يسترجع كائن [Border](../border/) حسب نوع الحد. |
| [idx_get](./idx_get/)(int32_t) | يسترجع كائن [Border](../border/) حسب الفهرس. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | محدد لـ [Aspose::Words::BorderCollection::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | محدد لـ [Aspose::Words::BorderCollection::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | محدد لـ [Aspose::Words::BorderCollection::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | محدد لـ [Aspose::Words::BorderCollection::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | المحدد لـ [Aspose::Words::BorderCollection::get_Shadow](./get_shadow/). |
| static [Type](./type/)() |  |

## أمثلة



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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
