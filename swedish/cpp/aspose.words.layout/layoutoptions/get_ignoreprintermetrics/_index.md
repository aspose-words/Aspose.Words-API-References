---
title: "Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics‑metod"
linktitle: "get_IgnorePrinterMetrics"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics‑metod. Hämtar eller anger indikation på om kompatibilitetsalternativet \"Use printer metrics to lay out document\" ignoreras. Standard är true i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.layout/layoutoptions/get_ignoreprintermetrics/
---
## LayoutOptions::get_IgnorePrinterMetrics method


Hämtar eller sätter indikation på om kompatibilitetsalternativet "Use printer metrics to lay out document" ignoreras. Standard är **true**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics() const
```


## Exempel



Visar hur du ignorerar alternativet 'Use printer metrics to lay out document'.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

doc->get_LayoutOptions()->set_IgnorePrinterMetrics(false);

doc->Save(get_ArtifactsDir() + u"Document.IgnorePrinterMetrics.docx");
```

## Se även

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
