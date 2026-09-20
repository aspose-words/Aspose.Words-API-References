---
title: "Método Aspose::Words::Document::get_ReadabilityStatistics"
linktitle: "get_ReadabilityStatistics"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::get_ReadabilityStatistics. Proporciona información de la puntuación de legibilidad del documento en C++."
type: docs
weight: 44750
url: /es/cpp/aspose.words/document/get_readabilitystatistics/
---
## Document::get_ReadabilityStatistics method


Proporciona información de puntuación de legibilidad para el documento.

```cpp
System::SharedPtr<Aspose::Words::ReadabilityStatistics> Aspose::Words::Document::get_ReadabilityStatistics()
```


## Ejemplos



Muestra cómo calcular y mostrar las puntuaciones de lectura Flesch para un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"The implementation of artificial intelligence algorithms requires a comprehensive understanding of machine learning methodologies and statistical analysis techniques.");
builder->Writeln(u"Furthermore, the integration of neural networks into existing software architectures presents significant challenges for developers.");
builder->Writeln(u"This document serves as an illustrative example for calculating readability metrics using the Flesch reading ease formula.");

// Calcule las estadísticas de legibilidad.
System::SharedPtr<Aspose::Words::ReadabilityStatistics> stats = doc->get_ReadabilityStatistics();
// Verifique que las puntuaciones estén dentro de los rangos válidos esperados.
// CSPORTCPP: Tipo de expresión no compatible Assert.That (stats.FleschReadingEasy, Is.GreaterThanOrEqualTo (0).And.LessThanOrEqualTo (190));
ASSERT_LE(stats->get_FleschKincaidGradeLevel(), 0);
```

## Ver también

* Class [ReadabilityStatistics](../../readabilitystatistics/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
