---
title: "Aspose::Words::Document::get_ReadabilityStatistics method"
linktitle: "get_ReadabilityStatistics"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_ReadabilityStatistics method. Tillhandahåller information om läsbarhetspoäng för dokumentet i C++."
type: docs
weight: 44750
url: /sv/cpp/aspose.words/document/get_readabilitystatistics/
---
## Document::get_ReadabilityStatistics method


Tillhandahåller information om läsbarhetspoäng för dokumentet.

```cpp
System::SharedPtr<Aspose::Words::ReadabilityStatistics> Aspose::Words::Document::get_ReadabilityStatistics()
```


## Exempel



Visar hur man beräknar och visar Flesch-läsresultaten för ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"The implementation of artificial intelligence algorithms requires a comprehensive understanding of machine learning methodologies and statistical analysis techniques.");
builder->Writeln(u"Furthermore, the integration of neural networks into existing software architectures presents significant challenges for developers.");
builder->Writeln(u"This document serves as an illustrative example for calculating readability metrics using the Flesch reading ease formula.");

// Beräkna läsbarhetsstatistik.
System::SharedPtr<Aspose::Words::ReadabilityStatistics> stats = doc->get_ReadabilityStatistics();
// Verifiera att resultaten ligger inom förväntade giltiga intervall.
// CSPORTCPP: Ostödd uttryckstyp Assert.That (stats.FleschReadingEasy, Is.GreaterThanOrEqualTo (0).And.LessThanOrEqualTo (190));
ASSERT_LE(stats->get_FleschKincaidGradeLevel(), 0);
```

## Se även

* Class [ReadabilityStatistics](../../readabilitystatistics/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
