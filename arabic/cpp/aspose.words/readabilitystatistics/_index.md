---
title: "Aspose::Words::ReadabilityStatistics class"
linktitle: "ReadabilityStatistics"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ReadabilityStatistics class. يوفر معلومات حول درجة قابلية قراءة المستند في C++."
type: docs
weight: 51500
url: /ar/cpp/aspose.words/readabilitystatistics/
---
## ReadabilityStatistics class


يوفر معلومات حول درجة قابلية قراءة المستند.

```cpp
class ReadabilityStatistics : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_FleschKincaidGradeLevel](./get_fleschkincaidgradelevel/)() | درجة مستوى الصف وفقًا لـ Flesch-Kincaid. |
| [get_FleschReadingEasy](./get_fleschreadingeasy/)() | درجة سهولة القراءة وفقًا لـ Flesch. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
