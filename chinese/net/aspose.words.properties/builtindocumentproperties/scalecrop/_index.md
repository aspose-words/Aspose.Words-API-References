---
title: BuiltInDocumentProperties.ScaleCrop
linktitle: ScaleCrop
articleTitle: ScaleCrop
second_title: Aspose.Words for .NET
description: 发现 BuiltInDocumentProperties 中的 ScaleCrop 属性，该属性控制缩略图显示 - 确保裁剪或缩放图像时获得最佳观看效果。
type: docs
weight: 260
url: /zh/net/aspose.words.properties/builtindocumentproperties/scalecrop/
---
## BuiltInDocumentProperties.ScaleCrop property

指示是否裁剪或缩放文档缩略图以适合显示。

```csharp
public bool ScaleCrop { get; }
```

## 评论

Aspose.Words 不会更新此属性。

## 例子

展示如何获取扩展属性。

```csharp
Document doc = new Document(MyDir + "Extended properties.docx");
Assert.IsTrue(doc.BuiltInDocumentProperties.ScaleCrop);
Assert.IsTrue(doc.BuiltInDocumentProperties.SharedDocument);
Assert.IsTrue(doc.BuiltInDocumentProperties.HyperlinksChanged);
```

### 也可以看看

* class [BuiltInDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)
