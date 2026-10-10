---
title: "طريقة Aspose::Words::Document::get_VersionsCount"
linktitle: "get_VersionsCount"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_VersionsCount. يحصل على عدد إصدارات المستند التي تم تخزينها في مستند DOC في C++."
type: docs
weight: 57000
url: /ar/cpp/aspose.words/document/get_versionscount/
---
## Document::get_VersionsCount method


يحصل على عدد إصدارات المستند التي تم تخزينها في مستند DOC.

```cpp
int32_t Aspose::Words::Document::get_VersionsCount()
```

## ملاحظات


يتم الوصول إلى الإصدارات في Microsoft Word عبر قائمة File/Versions. يدعم Microsoft Word الإصدارات فقط لملفات DOC.

تسمح هذه الخاصية بالكشف عما إذا كانت هناك إصدارات مستند مخزنة في هذا المستند قبل فتحه في Aspose.Words. لا يوفر Aspose.Words أي دعم آخر لإصدارات المستندات. إذا قمت بحفظ هذا المستند باستخدام Aspose.Words، سيتم حفظ المستند بدون إصدارات.

## أمثلة



يوضح كيفية العمل مع ميزة عدد الإصدارات في مستندات Microsoft Word القديمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Versions.doc");

// يمكننا قراءة هذه الخاصية من المستند، لكن لا يمكننا الحفاظ عليها أثناء الحفظ.
ASSERT_EQ(4, doc->get_VersionsCount());

doc->Save(get_ArtifactsDir() + u"Document.VersionsCount.doc");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.VersionsCount.doc");

ASSERT_EQ(0, doc->get_VersionsCount());
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
