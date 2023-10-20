---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: 用于 .NET 的 Aspose.Words
description: Document AttachedTemplate 财产. 获取或设置附加到文档的模板的完整路径 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

获取或设置附加到文档的模板的完整路径。

```csharp
public string AttachedTemplate { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentNullException | 如果您尝试设置为`无效的`价值。 |

## 评论

空字符串表示文档附加到普通模板。

## 例子

演示如何为没有附加模板的文档设置默认模板。

```csharp
Document doc = new Document();

// 启用自动样式更新，但不附加模板文档。
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// 由于没有模板文档，文档无处跟踪样式更改。
// 使用 SaveOptions 对象自动设置模板
// 如果我们正在保存的文档没有该文档。
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
