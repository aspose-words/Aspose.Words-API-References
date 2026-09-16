---
title: "Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel method"
linktitle: "get_CompressionLevel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel method. 指定用于保存文档的压缩级别。默认值在 C++ 中为 Normal。"
type: docs
weight: 2250
url: /zh/cpp/aspose.words.saving/xpssaveoptions/get_compressionlevel/
---
## XpsSaveOptions::get_CompressionLevel method


指定用于保存文档的压缩级别。默认值为 [Normal](../../compressionlevel/)。

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel() const
```


## 示例



展示如何在将文档保存为 XPS 格式时控制压缩级别。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// 创建一个 XpsSaveOptions 对象并设置压缩级别。
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## 另见

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
