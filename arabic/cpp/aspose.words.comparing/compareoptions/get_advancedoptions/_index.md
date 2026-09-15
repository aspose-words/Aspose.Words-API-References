---
title: "Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions طريقة"
linktitle: "get_AdvancedOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions طريقة. يحدد خيارات مقارنة متقدمة قد تساعد في إنتاج مخرجات مقارنة أكثر دقة في C++."
type: docs
weight: 2500
url: /ar/cpp/aspose.words.comparing/compareoptions/get_advancedoptions/
---
## CompareOptions::get_AdvancedOptions method


يحدد خيارات مقارنة متقدمة قد تساعد في إنتاج مخرجات مقارنة أكثر دقة.

```cpp
const System::SharedPtr<Aspose::Words::Comparing::AdvancedCompareOptions> & Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions() const
```


## أمثلة



يظهر كيفية مقارنة المستندات مع تجاهل معرف DML الفريد.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID original.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID compare.docx");

// بشكل افتراضي، لا يتجاهل Aspose.Words معرف DML الفريد، وكان عدد المراجعات 2.
// إذا كنا نتجاهل معرف DML الفريد، كان عدد المراجعات 0.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreDmlUniqueId(isIgnoreDmlUniqueId);

docA->Compare(docB, u"Aspose.Words", System::DateTime::get_Now(), compareOptions);

ASSERT_EQ(isIgnoreDmlUniqueId ? 0 : 2, docA->get_Revisions()->get_Count());
```

## انظر أيضًا

* Class [AdvancedCompareOptions](../../advancedcompareoptions/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
