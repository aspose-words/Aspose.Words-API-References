---
title: "Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat 方法"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat 方法。指定在使用此保存选项对象时文档将保存的格式。仅在 C++ 中可以是 Docling。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/doclingsaveoptions/get_saveformat/
---
## DoclingSaveOptions::get_SaveFormat method


指定在使用此保存选项对象时文档将保存的格式。只能是 [Docling](../../../aspose.words/saveformat/)。

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat() override
```


## 示例



展示如何将文档保存为 Docling JSON 格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::DoclingSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docling);
// 设置为 true 可渲染非图像形状并将其包含在输出中。
// 设置为 false（默认）可从输出中排除非图像形状。
saveOptions->set_RenderNonImageShapes(true);

doc->Save(get_ArtifactsDir() + u"Document.DoclingJson.json", saveOptions);
```

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
