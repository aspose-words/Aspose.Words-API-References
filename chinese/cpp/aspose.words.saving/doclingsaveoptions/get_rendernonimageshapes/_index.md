---
title: "Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes 方法"
linktitle: "get_RenderNonImageShapes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes 方法。获取或设置一个值，指示是否应在 C++ 中渲染非图像形状并将其写入输出的 Docling JSON 文档。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.saving/doclingsaveoptions/get_rendernonimageshapes/
---
## DoclingSaveOptions::get_RenderNonImageShapes method


获取或设置一个值，指示是否应渲染非图像形状并将其写入输出的 Docling JSON 文档。

```cpp
bool Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes() const
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

* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
