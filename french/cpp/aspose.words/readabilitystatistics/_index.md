---
title: "Aspose::Words::ReadabilityStatistics class"
linktitle: "ReadabilityStatistics"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ReadabilityStatistics class. Fournit des informations sur le score de lisibilité du document en C++."
type: docs
weight: 51500
url: /fr/cpp/aspose.words/readabilitystatistics/
---
## ReadabilityStatistics class


Fournit des informations sur le score de lisibilité du document.

```cpp
class ReadabilityStatistics : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_FleschKincaidGradeLevel](./get_fleschkincaidgradelevel/)() | Score de niveau de classe Flesch‑Kincaid. |
| [get_FleschReadingEasy](./get_fleschreadingeasy/)() | Score de facilité de lecture Flesch. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exemples



Montre comment calculer et afficher les scores de lecture Flesch pour un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"The implementation of artificial intelligence algorithms requires a comprehensive understanding of machine learning methodologies and statistical analysis techniques.");
builder->Writeln(u"Furthermore, the integration of neural networks into existing software architectures presents significant challenges for developers.");
builder->Writeln(u"This document serves as an illustrative example for calculating readability metrics using the Flesch reading ease formula.");

// Calculer les statistiques de lisibilité.
System::SharedPtr<Aspose::Words::ReadabilityStatistics> stats = doc->get_ReadabilityStatistics();
// Vérifiez que les scores se situent dans les plages valides attendues.
// CSPORTCPP: Type d’expression non pris en charge Assert.That (stats.FleschReadingEasy, Is.GreaterThanOrEqualTo (0).And.LessThanOrEqualTo (190));
ASSERT_LE(stats->get_FleschKincaidGradeLevel(), 0);
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
