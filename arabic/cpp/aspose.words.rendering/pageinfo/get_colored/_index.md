---
title: "طريقة Aspose::Words::Rendering::PageInfo::get_Colored"
linktitle: "get_Colored"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Rendering::PageInfo::get_Colored. تُرجع true إذا كانت الصفحة تحتوي على محتوى ملون في C++."
type: docs
weight: 1500
url: /ar/cpp/aspose.words.rendering/pageinfo/get_colored/
---
## PageInfo::get_Colored method


ترجع **true** إذا كانت الصفحة تحتوي على محتوى ملون.

```cpp
bool Aspose::Words::Rendering::PageInfo::get_Colored()
```


## أمثلة



يظهر كيفية التحقق مما إذا كانت الصفحة ملونة أم لا.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// تحقق من أن الصفحة الأولى من المستند غير ملونة.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## انظر أيضًا

* Class [PageInfo](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
