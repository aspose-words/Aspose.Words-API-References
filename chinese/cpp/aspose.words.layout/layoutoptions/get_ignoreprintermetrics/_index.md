---
title: "Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics 方法"
linktitle: "get_IgnorePrinterMetrics"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics 方法。获取或设置是否忽略 \"Use printer metrics to lay out document\" 兼容性选项的指示。默认在 C++ 中为 true。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.layout/layoutoptions/get_ignoreprintermetrics/
---
## LayoutOptions::get_IgnorePrinterMetrics method


获取或设置是否忽略 "Use printer metrics to lay out document" 兼容性选项的指示。默认值为 **true**。

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics() const
```


## 示例



展示如何忽略 "Use printer metrics to lay out document" 选项。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

doc->get_LayoutOptions()->set_IgnorePrinterMetrics(false);

doc->Save(get_ArtifactsDir() + u"Document.IgnorePrinterMetrics.docx");
```

## 另见

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
