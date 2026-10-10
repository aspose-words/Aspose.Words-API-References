---
title: "Aspose::Words::ReadabilityStatistics class"
linktitle: "ReadabilityStatistics"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ReadabilityStatistics class. Proporciona información sobre la puntuación de legibilidad del documento en C++."
type: docs
weight: 51500
url: /es/cpp/aspose.words/readabilitystatistics/
---
## ReadabilityStatistics class


Proporciona información sobre la puntuación de legibilidad del documento.

```cpp
class ReadabilityStatistics : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_FleschKincaidGradeLevel](./get_fleschkincaidgradelevel/)() | Puntuación de nivel de grado Flesch-Kincaid. |
| [get_FleschReadingEasy](./get_fleschreadingeasy/)() | Puntuación de facilidad de lectura Flesch. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
