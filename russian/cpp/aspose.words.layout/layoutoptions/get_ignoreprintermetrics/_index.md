---
title: "Метод Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics"
linktitle: "get_IgnorePrinterMetrics"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics метод. Получает или задает индикатор того, игнорируется ли совместимая опция \"Use printer metrics to lay out document\". По умолчанию true в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.layout/layoutoptions/get_ignoreprintermetrics/
---
## LayoutOptions::get_IgnorePrinterMetrics method


Получает или задает индикатор того, игнорируется ли параметр совместимости «Использовать метрики принтера для компоновки документа». По умолчанию **true**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics() const
```


## Примеры



Показывает, как игнорировать опцию 'Use printer metrics to lay out document'.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

doc->get_LayoutOptions()->set_IgnorePrinterMetrics(false);

doc->Save(get_ArtifactsDir() + u"Document.IgnorePrinterMetrics.docx");
```

## См. также

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
