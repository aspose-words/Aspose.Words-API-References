---
title: SaveOptions.DefaultTemplate
linktitle: DefaultTemplate
articleTitle: DefaultTemplate
second_title: Aspose.Words for .NET
description: 轻松管理您的保存选项！设置或获取默认模板路径和文件名，简化文档处理流程。立即优化您的工作流程！
type: docs
weight: 40
url: /zh/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

获取或设置默认模板的路径（包括文件名）。 此属性的默认值为**空字符串**(Empty ).

```csharp
public string DefaultTemplate { get; set; }
```

## 评论

如果指定，则此路径用于加载模板[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/)是`真的`, 但是[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/)是空的。

## 例子

展示如何为没有附加模板的文档设置默认模板。

```csharp
Document doc = new Document();

// 启用自动样式更新，但不附加模板文档。
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// 由于没有模板文档，文档无处跟踪样式变化。
// 使用 SaveOptions 对象自动设置模板
// 如果我们正在保存的文档没有该属性。
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
