---
title: "فئة Aspose::Words::Settings::ViewOptions"
linktitle: "ViewOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Settings::ViewOptions class. يوفر خيارات مختلفة تتحكم في كيفية عرض المستند في Microsoft Word. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.settings/viewoptions/
---
## ViewOptions class


يوفر خيارات مختلفة تتحكم في طريقة عرض المستند في Microsoft Word. لمعرفة المزيد، زر مقالة الوثائق [Work with Options and Appearance of Word Documents](https://docs.aspose.com/words/cpp/work-with-word-document-options-and-appearance/).

```cpp
class ViewOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_DisplayBackgroundShape](./get_displaybackgroundshape/)() const | يتحكم في عرض الشكل الخلفي في عرض تخطيط الطباعة. |
| [get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/)() const | يقوم بإيقاف عرض المسافة بين أعلى النص وحافة الصفحة العليا. |
| [get_FormsDesign](./get_formsdesign/)() const | يحدد ما إذا كان المستند في وضع تصميم النماذج. |
| [get_ViewType](./get_viewtype/)() const | يتحكم في وضع العرض في Microsoft Word. |
| [get_ZoomPercent](./get_zoompercent/)() const | يحصل أو يضبط النسبة المئوية التي تريد عرض مستندك بها. |
| [get_ZoomType](./get_zoomtype/)() const | يحصل أو يضبط قيمة التكبير بناءً على حجم النافذة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayBackgroundShape](./set_displaybackgroundshape/)(bool) | مُعيّن لـ [Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape](./get_displaybackgroundshape/). |
| [set_DoNotDisplayPageBoundaries](./set_donotdisplaypageboundaries/)(bool) | مُعيّن لـ [Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/). |
| [set_FormsDesign](./set_formsdesign/)(bool) | مُعيّن لـ [Aspose::Words::Settings::ViewOptions::get_FormsDesign](./get_formsdesign/). |
| [set_ViewType](./set_viewtype/)(Aspose::Words::Settings::ViewType) | مُعيّن لـ [Aspose::Words::Settings::ViewOptions::get_ViewType](./get_viewtype/). |
| [set_ZoomPercent](./set_zoompercent/)(int32_t) | مُعيّن لـ [Aspose::Words::Settings::ViewOptions::get_ZoomPercent](./get_zoompercent/). |
| [set_ZoomType](./set_zoomtype/)(Aspose::Words::Settings::ZoomType) | مُعيّن لـ [Aspose::Words::Settings::ViewOptions::get_ZoomType](./get_zoomtype/). |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية تعيين عامل تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند التحميل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(Aspose::Words::Settings::ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(Aspose::Words::Settings::ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(Aspose::Words::Settings::ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```


يظهر كيفية تعيين نوع تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند التحميل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// قم بتعيين الخاصية "ZoomType" إلى "ZoomType.PageWidth" للحصول على Microsoft Word
// لتكبير المستند تلقائيًا ليتناسب مع عرض الصفحة.
// قم بتعيين الخاصية "ZoomType" إلى "ZoomType.FullPage" للحصول على Microsoft Word
// لتكبير المستند تلقائيًا لجعل الصفحة الأولى بالكامل مرئية.
// قم بتعيين الخاصية "ZoomType" إلى "ZoomType.TextFit" للحصول على Microsoft Word
// لتكبير المستند تلقائيًا ليتناسب مع هوامش النص الداخلية للصفحة الأولى.
doc->get_ViewOptions()->set_ZoomType(zoomType);

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomType.doc");
```

## انظر أيضًا

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
