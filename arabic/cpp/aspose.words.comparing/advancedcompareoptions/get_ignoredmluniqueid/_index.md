---
title: "طريقة Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId"
linktitle: "get_IgnoreDmlUniqueId"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId. يحدد ما إذا كان يجب تجاهل الاختلاف في معرف فريد لـ DrawingML في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.comparing/advancedcompareoptions/get_ignoredmluniqueid/
---
## AdvancedCompareOptions::get_IgnoreDmlUniqueId method


يحدد ما إذا كان يجب تجاهل الاختلاف في المعرف الفريد لـ DrawingML.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId() const
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

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
