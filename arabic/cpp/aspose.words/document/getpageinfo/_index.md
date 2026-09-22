---
title: "طريقة Aspose::Words::Document::GetPageInfo"
linktitle: "GetPageInfo"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::GetPageInfo. تحصل على حجم الصفحة واتجاهها ومعلومات أخرى حول الصفحة قد تكون مفيدة للطباعة أو التصيير في C++."
type: docs
weight: 62000
url: /ar/cpp/aspose.words/document/getpageinfo/
---
## Document::GetPageInfo method


يحصل على حجم الصفحة واتجاهها ومعلومات أخرى حول الصفحة قد تكون مفيدة للطباعة أو العرض.

```cpp
System::SharedPtr<Aspose::Words::Rendering::PageInfo> Aspose::Words::Document::GetPageInfo(int32_t pageIndex)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| pageIndex | int32_t | مؤشر الصفحة بدءًا من الصفر. |

## أمثلة



يظهر كيفية التحقق مما إذا كانت الصفحة ملونة أم لا.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// تحقق من أن الصفحة الأولى من المستند غير ملونة.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## انظر أيضًا

* Class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
