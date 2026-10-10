---
title: "Aspose::Words::Document::RemoveBlankPages طريقة"
linktitle: "RemoveBlankPages"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Document::RemoveBlankPages طريقة. يزيل الصفحات الفارغة من المستند في C++."
type: docs
weight: 67500
url: /ar/cpp/aspose.words/document/removeblankpages/
---
## Document::RemoveBlankPages method


يزيل الصفحات الفارغة من المستند.

```cpp
System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::Document::RemoveBlankPages()
```


### ReturnValue

تم اعتبار قائمة أرقام الصفحات كفارغة وإزالتها.

## أمثلة



يوضح كيفية إزالة الصفحات الفارغة من المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Blank pages.docx");
ASSERT_EQ(2, doc->get_PageCount());
doc->RemoveBlankPages();
doc->UpdatePageLayout();
ASSERT_EQ(1, doc->get_PageCount());
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
