---
title: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent method"
linktitle: "get_ZoomPercent"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent method. يحصل على النسبة المئوية أو يضبطها التي تريد عرض مستندك بها في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.settings/viewoptions/get_zoompercent/
---
## ViewOptions::get_ZoomPercent method


يحصل أو يضبط النسبة المئوية التي تريد عرض مستندك بها.

```cpp
int32_t Aspose::Words::Settings::ViewOptions::get_ZoomPercent() const
```

## ملاحظات


على الرغم من أن Aspose.Words قادر على قراءة وكتابة هذا الخيار، فإن استخدامه يخص التطبيق. على سبيل المثال لا يحترم MS Word 2013 قيمة هذا الخيار.

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

## انظر أيضًا

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
