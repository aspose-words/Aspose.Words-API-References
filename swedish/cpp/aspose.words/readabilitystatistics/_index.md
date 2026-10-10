---
title: "Aspose::Words::ReadabilityStatistics class"
linktitle: "ReadabilityStatistics"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ReadabilityStatistics class. Tillhandahåller information om dokumentets läsbarhetspoäng i C++."
type: docs
weight: 51500
url: /sv/cpp/aspose.words/readabilitystatistics/
---
## ReadabilityStatistics class


Tillhandahåller information om dokumentets läsbarhetspoäng.

```cpp
class ReadabilityStatistics : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_FleschKincaidGradeLevel](./get_fleschkincaidgradelevel/)() | Flesch-Kincaid Grade Level‑poäng. |
| [get_FleschReadingEasy](./get_fleschreadingeasy/)() | Flesch Reading Easy‑poäng. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
