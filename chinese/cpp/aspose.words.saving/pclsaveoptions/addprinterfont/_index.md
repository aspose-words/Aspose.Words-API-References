---
title: "Aspose::Words::Saving::PclSaveOptions::AddPrinterFont 方法"
linktitle: "AddPrinterFont"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PclSaveOptions::AddPrinterFont 方法。该方法在 C++ 中添加由制造商上传到打印机的字体信息。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions::AddPrinterFont method


添加由制造商上传到打印机的字体信息。

```cpp
void Aspose::Words::Saving::PclSaveOptions::AddPrinterFont(const System::String &fontFullName, const System::String &fontPclName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fontFullName | const System::String\& | 字体的完整名称（例如 "Times New Roman Bold Italic"）。 |
| fontPclName | const System::String\& | 在 Pcl 文档中使用的字体名称。 |

## 示例



展示如何让打印机将特定字体的所有实例替换为另一种字体。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Courier");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->AddPrinterFont(u"Courier New", u"Courier");

// 打印此文档时，打印机将使用 "Courier New" 字体。
// 访问文档使用 "Courier" 字体的地方。
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

## 另见

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
