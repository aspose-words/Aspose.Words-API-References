---
title: "Aspose::Words::Document::get_ViewOptions طريقة"
linktitle: "get_ViewOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_ViewOptions. توفر خيارات للتحكم في كيفية عرض المستند في Microsoft Word باستخدام C++."
type: docs
weight: 58000
url: /ar/cpp/aspose.words/document/get_viewoptions/
---
## Document::get_ViewOptions method


يوفر خيارات للتحكم في طريقة عرض المستند في Microsoft Word.

```cpp
System::SharedPtr<Aspose::Words::Settings::ViewOptions> Aspose::Words::Document::get_ViewOptions()
```


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

* Class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
