---
title: Document.AutomaticallyUpdateStyles
second_title: Aspose.Words for .NET API 参考
description: Document 财产. 获取或设置一个标志指示每次在 MS Word 中打开文档时是否更新文档中的样式以匹配 附加模板中的样式
type: docs
weight: 30
url: /zh/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

获取或设置一个标志，指示每次在 MS Word 中打开文档时是否更新文档中的样式以匹配 附加模板中的样式。

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

### 例子

显示如何将模板附加到文档。

```csharp
Document doc = new Document();

// 默认情况下，Microsoft Word 文档附带一个名为“Normal.dotm”的附加模板。
// 空白 Aspose.Words 文档没有默认模板。
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// 附加一个模板，然后设置标志以应用样式更改
// 在模板中到我们文档中的样式。
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

显示如何为没有附加模板的文档设置默认模板。

```csharp
Document doc = new Document();

// 启用自动样式更新，但不附加模板文档。
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// 由于没有模板文档，因此文档无处跟踪样式更改。
// 使用 SaveOptions 对象自动设置模板
// 如果我们正在保存的文档没有。
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


