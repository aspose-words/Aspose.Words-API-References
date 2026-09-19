---
title: "Aspose::Words::ReadabilityStatistics class"
linktitle: "ReadabilityStatistics"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::ReadabilityStatistics. Fornisce informazioni sul punteggio di leggibilità del documento in C++."
type: docs
weight: 51500
url: /it/cpp/aspose.words/readabilitystatistics/
---
## ReadabilityStatistics class


Fornisce informazioni sul punteggio di leggibilità del documento.

```cpp
class ReadabilityStatistics : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_FleschKincaidGradeLevel](./get_fleschkincaidgradelevel/)() | Punteggio Flesch-Kincaid Grade Level. |
| [get_FleschReadingEasy](./get_fleschreadingeasy/)() | Punteggio Flesch Reading Easy. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
