---
title: "طريقة Aspose::Words::StyleCollection::ClearQuickStyleGallery"
linktitle: "ClearQuickStyleGallery"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::StyleCollection::ClearQuickStyleGallery. يزيل جميع الأنماط من لوحة معرض الأنماط السريعة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection::ClearQuickStyleGallery method


يزيل جميع الأنماط من لوحة معرض [Style](../../style/) السريعة.

```cpp
void Aspose::Words::StyleCollection::ClearQuickStyleGallery()
```


## أمثلة



يوضح كيفية إزالة الأنماط من لوحة معرض [Style](../../style/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
// لاحظ أن إزالة الأنماط تعمل فقط مع تنسيق DOCX في الوقت الحالي.
doc->get_Styles()->ClearQuickStyleGallery();

doc->Save(get_ArtifactsDir() + u"Styles.RemoveStylesFromStyleGallery.docx");
```

## انظر أيضًا

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
