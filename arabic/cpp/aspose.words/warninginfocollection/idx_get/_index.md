---
title: "Aspose::Words::WarningInfoCollection::idx_get طريقة"
linktitle: "idx_get"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::WarningInfoCollection::idx_get طريقة. يحصل على عنصر في الفهرس المحدد في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words/warninginfocollection/idx_get/
---
## WarningInfoCollection::idx_get method


يحصل على عنصر في الفهرس المحدد.

```cpp
System::SharedPtr<Aspose::Words::WarningInfo> Aspose::Words::WarningInfoCollection::idx_get(int32_t index)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | فهرس يبدأ من الصفر للعنصر. |

## أمثلة



يوضح كيفية الحصول على تحذيرات حول الصيغ غير المدعومة.
```cpp
auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_WarningCallback(warnings);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"FB2 document.fb2", loadOptions);

ASSERT_EQ(u"The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings->idx_get(0)->get_Description());
ASSERT_EQ(1, warnings->get_Count());
```

## انظر أيضًا

* Class [WarningInfo](../../warninginfo/)
* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
