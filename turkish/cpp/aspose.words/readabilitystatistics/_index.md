---
title: "Aspose::Words::ReadabilityStatistics class"
linktitle: "ReadabilityStatistics"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ReadabilityStatistics sınıfı. C++'de belge okunabilirlik puanı hakkında bilgi sağlar."
type: docs
weight: 51500
url: /tr/cpp/aspose.words/readabilitystatistics/
---
## ReadabilityStatistics class


Belge okunabilirlik puanı hakkında bilgi sağlar.

```cpp
class ReadabilityStatistics : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_FleschKincaidGradeLevel](./get_fleschkincaidgradelevel/)() | Flesch-Kincaid Sınıf Düzeyi puanı. |
| [get_FleschReadingEasy](./get_fleschreadingeasy/)() | Flesch Okuma Kolaylığı puanı. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Örnekler



Bir belge için Flesch okuma puanlarını nasıl hesaplayıp görüntüleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"The implementation of artificial intelligence algorithms requires a comprehensive understanding of machine learning methodologies and statistical analysis techniques.");
builder->Writeln(u"Furthermore, the integration of neural networks into existing software architectures presents significant challenges for developers.");
builder->Writeln(u"This document serves as an illustrative example for calculating readability metrics using the Flesch reading ease formula.");

// Okunabilirlik istatistiklerini hesaplayın.
System::SharedPtr<Aspose::Words::ReadabilityStatistics> stats = doc->get_ReadabilityStatistics();
// Puanların beklenen geçerli aralıklar içinde olduğunu doğrulayın.
// CSPORTCPP: Desteklenmeyen ifade türü Assert.That (stats.FleschReadingEasy, Is.GreaterThanOrEqualTo (0).And.LessThanOrEqualTo (190));
ASSERT_LE(stats->get_FleschKincaidGradeLevel(), 0);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
