---
title: Document.RemoveMacros
linktitle: RemoveMacros
articleTitle: RemoveMacros
second_title: 用于 .NET 的 Aspose.Words
description: Document RemoveMacros 方法. 从文档中删除所有宏VBA 项目以及工具栏和命令自定义 在 C#.
type: docs
weight: 670
url: /zh/net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

从文档中删除所有宏（VBA 项目）以及工具栏和命令自定义。

```csharp
public void RemoveMacros()
```

## 评论

通过从文档中删除所有宏，您可以确保文档不包含宏病毒。

## 例子

演示如何从文档中删除所有宏。

```csharp
Document doc = new Document(MyDir + "Macro.docm");

Assert.IsTrue(doc.HasMacros);
Assert.AreEqual("Project", doc.VbaProject.Name);

// 删除文档的 VBA 项目及其所有宏。
doc.RemoveMacros();

Assert.IsFalse(doc.HasMacros);
Assert.Null(doc.VbaProject);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
