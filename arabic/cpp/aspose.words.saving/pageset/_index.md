---
title: "فئة Aspose::Words::Saving::PageSet"
linktitle: "PageSet"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Saving::PageSet. تصف مجموعة عشوائية من الصفحات. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words.saving/pageset/
---
## PageSet class


يصف مجموعة عشوائية من الصفحات. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageSet : public System::Collections::Generic::IEnumerable<int32_t>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [get_All](./get_all/)() | يحصل على مجموعة تحتوي على جميع صفحات المستند بترتيبها الأصلي. |
| static [get_Even](./get_even/)() | يحصل على مجموعة تحتوي على جميع الصفحات الزوجية للمستند بترتيبها الأصلي. |
| static [get_Odd](./get_odd/)() | يحصل على مجموعة تحتوي على جميع الصفحات الفردية للمستند بترتيبها الأصلي. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSet](./pageset/)(int32_t) | ينشئ مجموعة صفحة واحدة بناءً على فهرس الصفحة الدقيق. |
| [PageSet](./pageset/)(const System::ArrayPtr\<int32_t\>\&) | ينشئ مجموعة صفحات بناءً على فهارس الصفحات الدقيقة. |
| [PageSet](./pageset/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) | ينشئ مجموعة صفحات بناءً على نطاقات. |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية تحويل صفحة واحدة من مستند إلى صورة JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// إنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها تلك الطريقة بتحويل المستند إلى صورة.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// عيّن "PageSet" إلى "1" لاختيار الصفحة الثانية عبر
// الفهرس الصفري لبدء تحويل المستند منه.
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// عند حفظ المستند بتنسيق JPEG، تقوم Aspose.Words بتحويل صفحة واحدة فقط.
// ستحتوي هذه الصورة على صفحة واحدة تبدأ من الصفحة الثانية،
// وهي ستكون مجرد الصفحة الثانية من المستند الأصلي.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
