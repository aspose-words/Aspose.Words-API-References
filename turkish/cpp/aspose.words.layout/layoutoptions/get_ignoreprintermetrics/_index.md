---
title: "Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics metodu"
linktitle: "get_IgnorePrinterMetrics"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics yöntemi. Belgeyi yerleştirmek için \\\"Use printer metrics to lay out document\\\" uyumluluk seçeneğinin göz ardı edilip edilmediğini gösteren değeri alır veya ayarlar. Varsayılan değer C++'ta true'dur."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.layout/layoutoptions/get_ignoreprintermetrics/
---
## LayoutOptions::get_IgnorePrinterMetrics method


\"Belgeyi yerleştirmek için yazıcı ölçümleri kullan\" uyumluluk seçeneğinin göz ardı edilip edilmediğini gösteren değeri alır veya ayarlar. Varsayılan **true**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics() const
```


## Örnekler



Belgeyi yerleştirmek için 'Use printer metrics to lay out document' seçeneğinin nasıl göz ardı edileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

doc->get_LayoutOptions()->set_IgnorePrinterMetrics(false);

doc->Save(get_ArtifactsDir() + u"Document.IgnorePrinterMetrics.docx");
```

## Ayrıca Bakınız

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
