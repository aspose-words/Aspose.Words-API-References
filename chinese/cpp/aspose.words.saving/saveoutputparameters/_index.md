---
title: "Aspose::Words::Saving::SaveOutputParameters 类"
linktitle: "SaveOutputParameters"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOutputParameters 类。此对象在文档保存后返回给调用方，并包含在保存操作期间生成或计算的其他信息。调用方可以使用或忽略此对象。欲了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 30000
url: /zh/cpp/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class


文档保存后，此对象会返回给调用方，并包含在保存操作期间生成或计算的其他信息。调用方可以使用或忽略此对象。要了解更多，请访问 [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) 文档文章。

```cpp
class SaveOutputParameters : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_ContentType](./get_contenttype/)() const | 返回标识已保存文档类型的 Content-Type 字符串（Internet Media Type）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## 示例



展示如何访问文档保存操作的输出参数。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// 在保存文档后，我们可以访问新创建的输出文档的 Internet Media Type（MIME 类型）。
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.doc");

ASSERT_EQ(u"application/msword", parameters->get_ContentType());

// 此属性会根据保存格式而变化。
parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.pdf");

ASSERT_EQ(u"application/pdf", parameters->get_ContentType());
```

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
