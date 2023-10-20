---
title: PageInfo.Colored
linktitle: Colored
articleTitle: Colored
second_title: 用于 .NET 的 Aspose.Words
description: PageInfo Colored 财产. 返回真的如果页面包含彩色内容 在 C#.
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

演示如何检查页面是否为彩色。

```csharp
Document doc = new Document(MyDir + "Document.docx");

// 检查文档的第一页是否未着色。
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### 也可以看看

* class [PageInfo](../)
* 命名空间 [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../../)
