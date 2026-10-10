---
title: "Aspose::Words::IDocumentProcessorPlugin 接口"
linktitle: "IDocumentProcessorPlugin"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::IDocumentProcessorPlugin 接口。定义了在 C++ 中用于外部文档处理插件的接口。"
type: docs
weight: 76750
url: /zh/cpp/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface


定义外部文档处理器插件的接口。

```cpp
class IDocumentProcessorPlugin : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [Append](./append/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | 使用指定的加载选项加载并追加文档。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Load](./load/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | 使用指定的加载选项加载文档。 |
| virtual [Save](./save/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | 使用指定的保存选项，将通过 [Load()](./load/) 方法加载的文档保存到输出流。 |
| virtual [SetImageWatermark](./setimagewatermark/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>) | 在通过 [Load()](./load/) 方法加载的文档的每一页上添加图片水印。 |
| virtual [SetTextWatermark](./settextwatermark/)(System::String, System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>) | 在通过 [Load()](./load/) 方法加载的文档的每一页上添加文字水印。 |
| virtual [ToDocument](./todocument/)() | 将通过 [Load()](./load/) 方法加载的文档解析为 [Document](../document/) 对象。 |
| virtual [ToPages](./topages/)(System::SharedPtr\<Aspose::Words::Saving::FixedPageSaveOptions\>) | 使用指定的固定页面保存选项，将通过 [Load()](./load/) 方法加载的文档的每一页保存。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
