---
title: "طريقة Aspose::Words::Lists::List::HasSameTemplate"
linktitle: "HasSameTemplate"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Lists::List::HasSameTemplate. تُرجع true إذا كانت القائمة الحالية والقائمة المعطاة مُنشأة من نفس القالب في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.lists/list/hassametemplate/
---
## List::HasSameTemplate method


يرجع true إذا تم إنشاء القائمة الحالية والقائمة المعطاة من نفس القالب.

```cpp
bool Aspose::Words::Lists::List::HasSameTemplate(const System::SharedPtr<Aspose::Words::Lists::List> &other)
```


## أمثلة



يظهر كيفية تعريف القوائم بنفس معرف ListDefId.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Different lists.docx");

ASSERT_TRUE(doc->get_Lists()->idx_get(0)->HasSameTemplate(doc->get_Lists()->idx_get(1)));
ASSERT_FALSE(doc->get_Lists()->idx_get(1)->HasSameTemplate(doc->get_Lists()->idx_get(2)));
```

## انظر أيضًا

* Class [List](../)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
