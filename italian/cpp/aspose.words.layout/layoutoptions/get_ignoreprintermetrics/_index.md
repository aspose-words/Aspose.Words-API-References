---
title: "Metodo Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics"
linktitle: "get_IgnorePrinterMetrics"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics. Ottiene o imposta l'indicazione se l'opzione di compatibilità \\\"Use printer metrics to lay out document\\\" è ignorata. Il valore predefinito è true in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.layout/layoutoptions/get_ignoreprintermetrics/
---
## LayoutOptions::get_IgnorePrinterMetrics method


Ottiene o imposta l'indicazione se l'opzione di compatibilità "Use printer metrics to lay out document" è ignorata. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics() const
```


## Esempi



Mostra come ignorare l'opzione 'Use printer metrics to lay out document'.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

doc->get_LayoutOptions()->set_IgnorePrinterMetrics(false);

doc->Save(get_ArtifactsDir() + u"Document.IgnorePrinterMetrics.docx");
```

## Vedi anche

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
