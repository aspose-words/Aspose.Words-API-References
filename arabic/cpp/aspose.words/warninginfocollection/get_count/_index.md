---
title: "Aspose::Words::WarningInfoCollection::get_Count طريقة"
linktitle: "get_Count"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::WarningInfoCollection::get_Count طريقة. يحصل على عدد العناصر الموجودة في المجموعة في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words/warninginfocollection/get_count/
---
## WarningInfoCollection::get_Count method


يحصل على عدد العناصر الموجودة في المجموعة.

```cpp
int32_t Aspose::Words::WarningInfoCollection::get_Count()
```


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

* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
