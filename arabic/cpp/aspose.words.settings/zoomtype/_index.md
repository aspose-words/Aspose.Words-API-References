---
title: "Aspose::Words::Settings::ZoomType enum"
linktitle: "ZoomType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Settings::ZoomType enum. القيم المحتملة لتحديد حجم ظهور المستند على الشاشة في Microsoft Word في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words.settings/zoomtype/
---
## ZoomType enum


القيم المحتملة لحجم ظهور المستند على الشاشة في Microsoft Word.

```cpp
enum class ZoomType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| مخصص | 0 | نسبة التكبير يتم تعيينها صراحة. لا يتم إعادة حسابها تلقائيًا عندما يتغير حجم التحكم. |
| None | n/a | يشير إلى استخدام نسبة التكبير الصريحة. نفس ما هو موجود في [مخصص](./). |
| FullPage | 1 | نسبة التكبير يتم إعادة حسابها تلقائيًا لتناسب صفحة كاملة واحدة. |
| PageWidth | 2 | نسبة التكبير يتم إعادة حسابها تلقائيًا لتناسب عرض الصفحة. |
| TextFit | 3 | نسبة التكبير يتم إعادة حسابها تلقائيًا لتناسب النص. |


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
