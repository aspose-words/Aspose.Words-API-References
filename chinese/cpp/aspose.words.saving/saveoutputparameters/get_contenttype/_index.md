---
title: "Aspose::Words::Saving::SaveOutputParameters::get_ContentType 方法"
linktitle: "get_ContentType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOutputParameters::get_ContentType 方法。返回 Content-Type 字符串（Internet Media Type），用于标识在 C++ 中保存的文档类型。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.saving/saveoutputparameters/get_contenttype/
---
## SaveOutputParameters::get_ContentType method


返回标识已保存文档类型的 Content-Type 字符串（Internet Media Type）。

```cpp
System::String Aspose::Words::Saving::SaveOutputParameters::get_ContentType() const
```


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

* Class [SaveOutputParameters](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
