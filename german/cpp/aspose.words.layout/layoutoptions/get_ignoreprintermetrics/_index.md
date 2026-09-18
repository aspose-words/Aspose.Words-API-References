---
title: "Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics Methode"
linktitle: "get_IgnorePrinterMetrics"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics Methode. Gibt an, ob die Kompatibilitätsoption \"Use printer metrics to lay out document\" ignoriert wird, oder legt dies fest. Der Standardwert ist true in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.layout/layoutoptions/get_ignoreprintermetrics/
---
## LayoutOptions::get_IgnorePrinterMetrics method


Liest oder schreibt die Angabe, ob die Kompatibilitätsoption \"Use printer metrics to lay out document\" ignoriert wird. Der Standardwert ist **true**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics() const
```


## Beispiele



Zeigt, wie man die Option 'Use printer metrics to lay out document' ignoriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

doc->get_LayoutOptions()->set_IgnorePrinterMetrics(false);

doc->Save(get_ArtifactsDir() + u"Document.IgnorePrinterMetrics.docx");
```

## Siehe auch

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
