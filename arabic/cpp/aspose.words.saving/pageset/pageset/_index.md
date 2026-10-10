---
title: "Aspose::Words::Saving::PageSet::PageSet منشئ"
linktitle: "PageSet"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::PageSet::PageSet منشئ. ينشئ مجموعة صفحات بناءً على مؤشرات الصفحات الدقيقة في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/pageset/pageset/
---
## PageSet::PageSet(const System::ArrayPtr\<int32_t\>\&) constructor


ينشئ مجموعة صفحات بناءً على فهارس الصفحات الدقيقة.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<int32_t> &pages)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| الصفحات | const System::ArrayPtr\<int32_t\>\& | مؤشرات الصفحات التي تبدأ من الصفر. |

## أمثلة



يوضح كيفية استخراج الصفحات بناءً على مؤشرات الصفحات الدقيقة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أضف خمس صفحات إلى المستند.
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// أنشئ كائن "XpsSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل تلك الطريقة للمستند إلى .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// استخدم الخاصية "PageSet" لتحديد مجموعة من صفحات المستند لحفظها في XPS الناتج.
// في هذه الحالة، سنختار، عبر فهرس يبدأ من الصفر، ثلاث صفحات فقط: الصفحة 1، الصفحة 2، والصفحة 4.
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## انظر أيضًا

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) constructor


ينشئ مجموعة صفحات بناءً على نطاقات.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Saving::PageRange>> &ranges)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| النطاقات | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\& | مصفوفة من نطاقات الصفحات. |

## أمثلة



يوضح كيفية استخراج الصفحات بناءً على نطاقات صفحات دقيقة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## انظر أيضًا

* Class [PageRange](../../pagerange/)
* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(int32_t) constructor


ينشئ مجموعة صفحة واحدة بناءً على فهرس الصفحة الدقيق.

```cpp
Aspose::Words::Saving::PageSet::PageSet(int32_t page)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| الصفحة | int32_t | مؤشر الصفحة التي تبدأ من الصفر. |

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

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
