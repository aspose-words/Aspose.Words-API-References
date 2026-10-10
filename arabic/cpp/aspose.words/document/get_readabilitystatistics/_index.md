---
title: "طريقة Aspose::Words::Document::get_ReadabilityStatistics"
linktitle: "get_ReadabilityStatistics"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_ReadabilityStatistics. توفر معلومات عن درجة قابلية القراءة للمستند في C++."
type: docs
weight: 44750
url: /ar/cpp/aspose.words/document/get_readabilitystatistics/
---
## Document::get_ReadabilityStatistics method


يوفر معلومات عن درجة قابلية القراءة للمستند.

```cpp
System::SharedPtr<Aspose::Words::ReadabilityStatistics> Aspose::Words::Document::get_ReadabilityStatistics()
```


## أمثلة



يوضح كيفية حساب وعرض درجات القراءة وفقًا لـ Flesch لمستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"The implementation of artificial intelligence algorithms requires a comprehensive understanding of machine learning methodologies and statistical analysis techniques.");
builder->Writeln(u"Furthermore, the integration of neural networks into existing software architectures presents significant challenges for developers.");
builder->Writeln(u"This document serves as an illustrative example for calculating readability metrics using the Flesch reading ease formula.");

// احسب إحصاءات قابلية القراءة.
System::SharedPtr<Aspose::Words::ReadabilityStatistics> stats = doc->get_ReadabilityStatistics();
// تحقق من أن الدرجات ضمن النطاقات الصالحة المتوقعة.
// CSPORTCPP: نوع تعبير غير مدعوم Assert.That (stats.FleschReadingEasy, Is.GreaterThanOrEqualTo (0).And.LessThanOrEqualTo (190));
ASSERT_LE(stats->get_FleschKincaidGradeLevel(), 0);
```

## انظر أيضًا

* Class [ReadabilityStatistics](../../readabilitystatistics/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
