---
title: "تعداد Aspose::Words::Settings::ViewType"
linktitle: "ViewType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::Settings::ViewType. القيم المحتملة لوضع العرض في Microsoft Word في C++."
type: docs
weight: 21000
url: /ar/cpp/aspose.words.settings/viewtype/
---
## ViewType enum


القيم المحتملة لوضع العرض في Microsoft Word.

```cpp
enum class ViewType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | يجب عرض المستند في العرض الافتراضي للتطبيق. |
| Reading | 0 | يجب عرض المستند في العرض الافتراضي للتطبيق. |
| PageLayout | 1 | يجب فتح المستند في عرض يُظهر المستند كما سيُطبع. |
| Outline | 3 | يجب عرض المستند في عرض مُحسّن للتخطيط أو لإنشاء مستندات طويلة. |
| عادي | 4 | يجب عرض المستند في عرض مُحسّن للتخطيط أو لإنشاء مستندات طويلة. |
| Web | 5 | يجب عرض المستند في عرض يحاكي الطريقة التي سيُعرض بها هذا المستند في صفحة ويب. |


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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
