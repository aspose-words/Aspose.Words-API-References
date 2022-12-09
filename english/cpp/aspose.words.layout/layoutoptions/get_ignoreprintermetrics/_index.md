---
title: get_IgnorePrinterMetrics
second_title: Aspose.Words for C++ API Reference
description: Gets or sets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. Default is true.
type: docs
weight: 66
url: /cpp/aspose.words.layout/layoutoptions/get_ignoreprintermetrics/
---
## LayoutOptions::get_IgnorePrinterMetrics method


Gets or sets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. Default is **true**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics() const
```


## Examples



Shows how to ignore 'Use printer metrics to lay out document' option. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

doc->get_LayoutOptions()->set_IgnorePrinterMetrics(false);

doc->Save(ArtifactsDir + u"Document.IgnorePrinterMetrics.docx");
```

## See Also

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words](../../../)
