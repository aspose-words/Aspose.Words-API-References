---
title: "Aspose::Words::Document::get_ReadabilityStatistics Methode"
linktitle: "get_ReadabilityStatistics"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_ReadabilityStatistics Methode. Liefert Lesbarkeitsbewertungsinformationen für das Dokument in C++."
type: docs
weight: 44750
url: /de/cpp/aspose.words/document/get_readabilitystatistics/
---
## Document::get_ReadabilityStatistics method


Stellt Informationen zum Lesbarkeitswert des Dokuments bereit.

```cpp
System::SharedPtr<Aspose::Words::ReadabilityStatistics> Aspose::Words::Document::get_ReadabilityStatistics()
```


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

* Class [ReadabilityStatistics](../../readabilitystatistics/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
