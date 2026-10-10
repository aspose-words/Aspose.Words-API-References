---
title: "Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName 方法"
linktitle: "get_FallbackFontName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName 方法。该字体的名称将在打印机和内置字体集合中未找到预期字体时使用，适用于 C++。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/pclsaveoptions/get_fallbackfontname/
---
## PclSaveOptions::get_FallbackFontName method


如果在打印机和内置字体集合中未找到预期的字体，将使用的字体名称。

```cpp
System::String Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName() const
```


## 示例



展示如何声明一种字体，以便在原始字体不可用时，打印机将其作为替代应用于打印文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_FallbackFontName(u"Times New Roman");

// 此文档将指示打印机将 "Times New Roman" 应用于缺少字体的文本。
// 如果 "Times New Roman" 也不可用，打印机将默认使用 "Arial" 字体。
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

## 另见

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
