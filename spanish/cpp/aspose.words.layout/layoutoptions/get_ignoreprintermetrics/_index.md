---
title: "Método Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics"
linktitle: "get_IgnorePrinterMetrics"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics método. Obtiene o establece la indicación de si la opción de compatibilidad \"Use printer metrics to lay out document\" se ignora. El valor predeterminado es true en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.layout/layoutoptions/get_ignoreprintermetrics/
---
## LayoutOptions::get_IgnorePrinterMetrics method


Obtiene o establece la indicación de si se ignora la opción de compatibilidad "Usar métricas de impresora para diseñar el documento". El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics() const
```


## Ejemplos



Muestra cómo ignorar la opción 'Use printer metrics to lay out document'.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

doc->get_LayoutOptions()->set_IgnorePrinterMetrics(false);

doc->Save(get_ArtifactsDir() + u"Document.IgnorePrinterMetrics.docx");
```

## Ver también

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
