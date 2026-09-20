---
title: "Aspose::Words::IDocumentConverterPlugin 接口"
linktitle: "IDocumentConverterPlugin"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::IDocumentConverterPlugin 接口。定义了 C++ 中外部转换插件的接口。"
type: docs
weight: 76250
url: /zh/cpp/aspose.words/idocumentconverterplugin/
---
## IDocumentConverterPlugin interface


定义外部转换器插件的接口。

```cpp
class IDocumentConverterPlugin : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [Convert](./convert/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | 使用指定的输入输出流和保存选项转换文档。 |
| virtual [ConvertToImages](./converttoimages/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | 将文档的页面从输入流转换为图像数组。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
