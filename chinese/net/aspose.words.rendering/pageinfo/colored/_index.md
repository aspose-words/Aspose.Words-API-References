---
title: PageInfo.Colored
linktitle: Colored
articleTitle: Colored
second_title: Aspose.Words for .NET
description: 使用 PageInfo Colored 属性，探索您的页面是否包含鲜艳的彩色内容。增强用户参与度并提升视觉吸引力！
type: docs
weight: 10
url: /zh/net/aspose.words.rendering/pageinfo/colored/
---
## PageInfo.Colored property

返回`真的`如果页面包含彩色内容。

```csharp
public bool Colored { get; }
```

## 例子

显示如何检查页面是否为彩色。

```csharp
Document doc = new Document(MyDir + "Document.docx");

// 检查文档的第一页是否没有彩色。
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### 也可以看看

* class [PageInfo](../)
* 命名空间 [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../../)
