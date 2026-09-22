---
title: "Aspose::Words::Comparing::Granularity enum"
linktitle: "Granularity"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Comparing::Granularity enum. يحدد درجة تفصيل التغييرات التي يجب تتبعها عند مقارنة مستندين في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.comparing/granularity/
---
## Granularity enum


يحدد درجة تفصيل التغييرات التي يجب تتبعها عند مقارنة مستندين.

```cpp
enum class Granularity
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| CharLevel | 0 | يحدد التغييرات على مستوى الأحرف. |
| WordLevel | 1 | يحدد التغييرات على مستوى الكلمات. |


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

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
