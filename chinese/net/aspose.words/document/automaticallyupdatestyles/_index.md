---
title: Document.AutomaticallyUpdateStyles
linktitle: AutomaticallyUpdateStyles
articleTitle: AutomaticallyUpdateStyles
second_title: Aspose.Words for .NET
description: 了解 MS Word 中的 AutomaticallyUpdateStyles 属性如何确保每次打开文档时文档的样式都与模板同步，从而增强一致性。
type: docs
weight: 30
url: /zh/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

获取或设置一个标志，指示每次在 MS Word 中打开文档时，文档中的样式是否更新以匹配 附加模板中的样式。

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

## 例子

展示如何将模板附加到文档。

```csharp
Document doc = new Document();

// Microsoft Word 文档默认附带一个名为“Normal.dotm”的附加模板。
// 空白 Aspose.Words 文档没有默认模板。
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// 附加模板，然后设置标志以应用样式更改
// 在模板内将样式添加到我们的文档中。
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

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

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
