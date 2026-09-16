---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri 方法"
linktitle: "get_ResourceFileUri"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri 方法。获取或设置用于从文档引用资源文件的统一资源标识符（URI），在 C++ 中使用。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/resourcesavingargs/get_resourcefileuri/
---
## ResourceSavingArgs::get_ResourceFileUri method


获取或设置用于从文档引用资源文件的统一资源标识符（URI）。

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri() const
```

## 备注


此属性允许您更改导出为固定页面 HTML、SVG 或 Markdown 文档的资源文件的 URI。

Aspose.Words 在导出为固定页面 HTML、SVG 或 Markdown 格式时，会自动为每个资源文件生成一个 URI。生成的 URI 引用由 Aspose.Words 保存的资源文件。但是，如果资源文件被移动到其他位置或保存到流中，URI 可能不正确。此属性可在这些情况下纠正 URI。

当事件触发时，此属性包含由 Aspose.Words 生成的 URI。您可以更改此属性的值，为资源文件提供自定义 URI。
## 另见

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
