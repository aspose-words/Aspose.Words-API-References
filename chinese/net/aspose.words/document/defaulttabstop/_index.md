---
title: Document.DefaultTabStop
linktitle: DefaultTabStop
articleTitle: DefaultTabStop
second_title: Aspose.Words for .NET
description: 了解如何自定义 DefaultTabStop 属性以设置精确的制表符间隔（以点为单位），从而增强文档格式和布局。
type: docs
weight: 100
url: /zh/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

获取或设置默认制表位之间的间隔（以点为单位）。

```csharp
public double DefaultTabStop { get; set; }
```

## 例子

展示如何设置制表位位置的自定义间隔。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 设置制表位每 72 点（1 英寸）出现一次。
builder.Document.DefaultTabStop = 72;

// 每个制表符都会将其后的文本对齐到下一个最近的制表位位置。
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### 也可以看看

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
