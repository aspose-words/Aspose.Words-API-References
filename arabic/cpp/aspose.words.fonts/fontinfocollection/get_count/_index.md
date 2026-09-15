---
title: "طريقة Aspose::Words::Fonts::FontInfoCollection::get_Count"
linktitle: "get_Count"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::FontInfoCollection::get_Count. يحصل على عدد العناصر الموجودة في المجموعة في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.fonts/fontinfocollection/get_count/
---
## FontInfoCollection::get_Count method


يحصل على عدد العناصر الموجودة في المجموعة.

```cpp
int32_t Aspose::Words::Fonts::FontInfoCollection::get_Count()
```


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
