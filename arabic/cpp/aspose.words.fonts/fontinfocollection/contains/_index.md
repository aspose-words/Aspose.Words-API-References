---
title: "طريقة Aspose::Words::Fonts::FontInfoCollection::Contains"
linktitle: "Contains"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::FontInfoCollection::Contains. تحدد ما إذا كانت المجموعة تحتوي على خط بالاسم المحدد في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection::Contains method


يحدد ما إذا كانت المجموعة تحتوي على خط بالاسم المحدد.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::Contains(const System::String &name)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| name | const System::String\& | اسم الخط غير حساس لحالة الأحرف لتحديده. |

### ReturnValue

**true** if the item is found in the collection; otherwise, **false**.

## أمثلة



يعرض معلومات حول الخطوط الموجودة في المستند الفارغ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// يحتوي المستند الفارغ على 3 خطوط افتراضية. كل خط في المستند
// سيكون له كائن FontInfo المقابل الذي يحتوي على تفاصيل حول ذلك الخط.
ASSERT_EQ(3, doc->get_FontInfos()->get_Count());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Times New Roman"));
ASSERT_EQ(204, doc->get_FontInfos()->idx_get(u"Times New Roman")->get_Charset());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Symbol"));
ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Arial"));
```

## انظر أيضًا

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
