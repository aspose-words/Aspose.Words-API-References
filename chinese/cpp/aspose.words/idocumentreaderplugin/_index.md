---
title: "Aspose::Words::IDocumentReaderPlugin interface"
linktitle: "IDocumentReaderPlugin"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::IDocumentReaderPlugin 接口。定义一个用于外部读取插件的接口，可在 C++ 中将文件读取为文档。"
type: docs
weight: 77000
url: /zh/cpp/aspose.words/idocumentreaderplugin/
---
## IDocumentReaderPlugin interface


定义可将文件读取为文档的外部读取器插件的接口。

```cpp
class IDocumentReaderPlugin : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Read](./read/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Document\>) | 将指定流中的数据读取到 [Document](../document/) 实例中。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
