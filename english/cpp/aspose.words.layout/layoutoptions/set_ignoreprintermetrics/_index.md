---
title: Aspose::Words::Layout::LayoutOptions::set_IgnorePrinterMetrics method
linktitle: set_IgnorePrinterMetrics
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::LayoutOptions::set_IgnorePrinterMetrics method. Sets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. Default is true in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.layout/layoutoptions/set_ignoreprintermetrics/
---
## LayoutOptions::set_IgnorePrinterMetrics method


Sets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. Default is **true**.

```cpp
void Aspose::Words::Layout::LayoutOptions::set_IgnorePrinterMetrics(bool value)
```

## Examples


Shows how to ignore 'Use printer metrics to lay out document' option.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rendering.docx"));

doc->get_LayoutOptions()->set_IgnorePrinterMetrics(false);

doc->Save(get_ArtifactsDir() + u"Document.IgnorePrinterMetrics.docx");
```
## See Also

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
