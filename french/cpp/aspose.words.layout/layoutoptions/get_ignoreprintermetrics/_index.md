---
title: "Méthode Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics"
linktitle: "get_IgnorePrinterMetrics"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics méthode. Obtient ou définit l'indication de savoir si l'option de compatibilité \"Use printer metrics to lay out document\" est ignorée. La valeur par défaut est true en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.layout/layoutoptions/get_ignoreprintermetrics/
---
## LayoutOptions::get_IgnorePrinterMetrics method


Obtient ou définit l'indication de savoir si l'option de compatibilité « Utiliser les métriques de l'imprimante pour mettre en page le document » est ignorée. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics() const
```


## Exemples



Montre comment ignorer l'option 'Use printer metrics to lay out document'.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

doc->get_LayoutOptions()->set_IgnorePrinterMetrics(false);

doc->Save(get_ArtifactsDir() + u"Document.IgnorePrinterMetrics.docx");
```

## Voir aussi

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
