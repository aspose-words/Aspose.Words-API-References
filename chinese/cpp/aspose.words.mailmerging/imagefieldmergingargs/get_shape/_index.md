---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape 方法"
linktitle: "get_Shape"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape 方法。指定邮件合并引擎在 C++ 中必须插入到文档的形状。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.mailmerging/imagefieldmergingargs/get_shape/
---
## ImageFieldMergingArgs::get_Shape method


指定邮件合并引擎必须插入到文档中的形状。

```cpp
const System::SharedPtr<Aspose::Words::Drawing::Shape> & Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape() const
```

## 备注


当指定此属性时，邮件合并引擎会忽略所有其他属性，如 [ImageFileName](../get_imagefilename/) 或 [ImageStream](../get_imagestream/)，并直接将形状插入到文档中。

使用此属性可以完全控制图像合并字段的合并过程。例如，您可以指定 [WrapType](../../../aspose.words.drawing/shapebase/get_wraptype/) 或任何其他形状属性，以微调生成的节点。但请注意，您需要自行提供形状的内容。
## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [ImageFieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
