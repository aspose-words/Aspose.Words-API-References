---
title: "Aspose::Words::Document::get_ReadabilityStatistics method"
linktitle: "get_ReadabilityStatistics"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_ReadabilityStatistics method. Fournit des informations sur le score de lisibilité du document en C++."
type: docs
weight: 44750
url: /fr/cpp/aspose.words/document/get_readabilitystatistics/
---
## Document::get_ReadabilityStatistics method


Fournit des informations sur le score de lisibilité du document.

```cpp
System::SharedPtr<Aspose::Words::ReadabilityStatistics> Aspose::Words::Document::get_ReadabilityStatistics()
```


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

* Class [ReadabilityStatistics](../../readabilitystatistics/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
