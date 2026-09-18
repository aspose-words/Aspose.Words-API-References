---
title: "Aspose::Words::ReadabilityStatistics class"
linktitle: "ReadabilityStatistics"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ReadabilityStatistics class. Stellt Informationen über den Lesbarkeitswert eines Dokuments in C++ bereit."
type: docs
weight: 51500
url: /de/cpp/aspose.words/readabilitystatistics/
---
## ReadabilityStatistics class


Bietet Informationen über die Lesbarkeitsbewertung des Dokuments.

```cpp
class ReadabilityStatistics : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_FleschKincaidGradeLevel](./get_fleschkincaidgradelevel/)() | Flesch‑Kincaid-Gradniveau‑Punktzahl. |
| [get_FleschReadingEasy](./get_fleschreadingeasy/)() | Flesch Reading Easy‑Punktzahl. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man die Flesch-Lesbarkeitswerte für ein Dokument berechnet und anzeigt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"The implementation of artificial intelligence algorithms requires a comprehensive understanding of machine learning methodologies and statistical analysis techniques.");
builder->Writeln(u"Furthermore, the integration of neural networks into existing software architectures presents significant challenges for developers.");
builder->Writeln(u"This document serves as an illustrative example for calculating readability metrics using the Flesch reading ease formula.");

// Berechnen Sie Lesbarkeitsstatistiken.
System::SharedPtr<Aspose::Words::ReadabilityStatistics> stats = doc->get_ReadabilityStatistics();
// Verifizieren Sie, dass die Werte innerhalb der erwarteten gültigen Bereiche liegen.
// CSPORTCPP: Nicht unterstützter Ausdruckstyp Assert.That (stats.FleschReadingEasy, Is.GreaterThanOrEqualTo (0).And.LessThanOrEqualTo (190));
ASSERT_LE(stats->get_FleschKincaidGradeLevel(), 0);
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
