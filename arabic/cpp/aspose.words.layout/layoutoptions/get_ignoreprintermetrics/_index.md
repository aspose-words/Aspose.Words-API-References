---
title: "طريقة Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics"
linktitle: "get_IgnorePrinterMetrics"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics طريقة. يحصل أو يضبط إشارة إلى ما إذا كان خيار التوافق \"Use printer metrics to lay out document\" يتم تجاهله. القيمة الافتراضية هي true في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.layout/layoutoptions/get_ignoreprintermetrics/
---
## LayoutOptions::get_IgnorePrinterMetrics method


يحصل أو يعيّن إشارة ما إذا كان خيار التوافق "استخدام مقاييس الطابعة لتنسيق المستند" يتم تجاهله. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics() const
```


## أمثلة



يعرض كيفية تجاهل خيار 'Use printer metrics to lay out document'.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

doc->get_LayoutOptions()->set_IgnorePrinterMetrics(false);

doc->Save(get_ArtifactsDir() + u"Document.IgnorePrinterMetrics.docx");
```

## انظر أيضًا

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
