---
title: ImageFieldMergingArgs.Shape
linktitle: Shape
articleTitle: Shape
second_title: 用于 .NET 的 Aspose.Words
description: ImageFieldMergingArgs Shape 财产. 指定邮件合并引擎必须插入到文档中的形状 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.mailmerging/imagefieldmergingargs/shape/
---
## ImageFieldMergingArgs.Shape property

指定邮件合并引擎必须插入到文档中的形状。

```csharp
public Shape Shape { get; set; }
```

## 评论

指定此属性时，邮件合并引擎会忽略所有其他属性，例如[`ImageFileName`](../imagefilename/)或者[`ImageStream`](../imagestream/) 并简单地将形状插入到文档中。

使用此属性可以完全控制合并图像合并字段的过程。 例如，您可以指定[`WrapType`](../../../aspose.words.drawing/shapebase/wraptype/)或任何其他形状属性来微调结果节点。但是，请注意 您有责任提供形状的内容。

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [ImageFieldMergingArgs](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
