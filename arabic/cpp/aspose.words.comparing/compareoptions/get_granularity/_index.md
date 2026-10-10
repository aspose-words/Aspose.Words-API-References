---
title: "Aspose::Words::Comparing::CompareOptions::get_Granularity طريقة"
linktitle: "get_Granularity"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Comparing::CompareOptions::get_Granularity طريقة. يحدد ما إذا كانت التغييرات تُتبع حسب الحرف أو حسب الكلمة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.comparing/compareoptions/get_granularity/
---
## CompareOptions::get_Granularity method


يحدد ما إذا كانت التغييرات تُتبع حسب الحرف أو حسب الكلمة.

```cpp
Aspose::Words::Comparing::Granularity Aspose::Words::Comparing::CompareOptions::get_Granularity() const
```


## أمثلة



يعرض كيفية تحديد الدقة أثناء مقارنة المستندات.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>();
auto builderA = System::MakeObject<Aspose::Words::DocumentBuilder>(docA);
builderA->Writeln(u"Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

auto docB = System::MakeObject<Aspose::Words::Document>();
auto builderB = System::MakeObject<Aspose::Words::DocumentBuilder>(docB);
builderB->Writeln(u"Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// حدد ما إذا كانت التغييرات يتم تتبعها
// حسب الأحرف ('Granularity.CharLevel')، أو حسب الكلمات ('Granularity.WordLevel').
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_Granularity(granularity);

docA->Compare(docB, u"author", System::DateTime::get_Now(), compareOptions);

// تحتوي مجموعة مجموعات المراجعة في المستند الأول على جميع الاختلافات بين المستندات.
System::SharedPtr<Aspose::Words::RevisionGroupCollection> groups = docA->get_Revisions()->get_Groups();
ASSERT_EQ(5, groups->get_Count());
```

## انظر أيضًا

* Enum [Granularity](../../granularity/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
