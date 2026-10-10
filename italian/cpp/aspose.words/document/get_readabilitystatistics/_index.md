---
title: "Aspose::Words::Document::get_ReadabilityStatistics metodo"
linktitle: "get_ReadabilityStatistics"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_ReadabilityStatistics metodo. Fornisce informazioni sul punteggio di leggibilità del documento in C++."
type: docs
weight: 44750
url: /it/cpp/aspose.words/document/get_readabilitystatistics/
---
## Document::get_ReadabilityStatistics method


Fornisce informazioni sul punteggio di leggibilità per il documento.

```cpp
System::SharedPtr<Aspose::Words::ReadabilityStatistics> Aspose::Words::Document::get_ReadabilityStatistics()
```


## Esempi



Mostra come calcolare e visualizzare i punteggi di lettura Flesch per un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"The implementation of artificial intelligence algorithms requires a comprehensive understanding of machine learning methodologies and statistical analysis techniques.");
builder->Writeln(u"Furthermore, the integration of neural networks into existing software architectures presents significant challenges for developers.");
builder->Writeln(u"This document serves as an illustrative example for calculating readability metrics using the Flesch reading ease formula.");

// Calcola le statistiche di leggibilità.
System::SharedPtr<Aspose::Words::ReadabilityStatistics> stats = doc->get_ReadabilityStatistics();
// Verifica che i punteggi siano entro gli intervalli validi previsti.
// CSPORTCPP: Tipo di espressione non supportato Assert.That (stats.FleschReadingEasy, Is.GreaterThanOrEqualTo (0).And.LessThanOrEqualTo (190));
ASSERT_LE(stats->get_FleschKincaidGradeLevel(), 0);
```

## Vedi anche

* Class [ReadabilityStatistics](../../readabilitystatistics/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
