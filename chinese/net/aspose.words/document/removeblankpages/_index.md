---
title: Document.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words for .NET
description: 使用 RemoveBlankPages 方法轻松增强您的文档，消除不需要的空白页，获得精美、专业的效果。
type: docs
weight: 700
url: /zh/net/aspose.words/document/removeblankpages/
---
## Document.RemoveBlankPages method

从文档中删除空白页。

```csharp
public List<int> RemoveBlankPages()
```

### 返回值

页码列表已被视为空白并被删除。

## 评论

生成的文档将不包含被视为空白的页面，而其他内容（包括编号、页眉/页脚和整体布局）应保持不变。 当页面主体没有可见内容时，页面将被视为空白，例如， 没有边框的空表格将被视为不可见，因此页面将被检测为空白。

## 例子

展示如何从文档中删除空白页。

```csharp
Document doc = new Document(MyDir + "Blank pages.docx");
Assert.AreEqual(2, doc.PageCount);
doc.RemoveBlankPages();
doc.UpdatePageLayout();
Assert.AreEqual(1, doc.PageCount);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
