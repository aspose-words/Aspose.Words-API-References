---
title: "Aspose::Words::Document::get_ReadabilityStatistics yöntemi"
linktitle: "get_ReadabilityStatistics"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_ReadabilityStatistics yöntemi. Belge için C++ içinde okunabilirlik puanı bilgileri sağlar."
type: docs
weight: 44750
url: /tr/cpp/aspose.words/document/get_readabilitystatistics/
---
## Document::get_ReadabilityStatistics method


Belge için okunabilirlik puanı bilgisi sağlar.

```cpp
System::SharedPtr<Aspose::Words::ReadabilityStatistics> Aspose::Words::Document::get_ReadabilityStatistics()
```


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

* Class [ReadabilityStatistics](../../readabilitystatistics/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
