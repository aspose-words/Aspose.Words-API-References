---
title: Document.DefaultTabStop
linktitle: DefaultTabStop
articleTitle: DefaultTabStop
second_title: 用于 .NET 的 Aspose.Words
description: Document DefaultTabStop 财产. 获取或设置默认制表位之间的间隔以磅为单位 在 C#.
type: docs
weight: 90
url: /zh/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

获取或设置默认制表位之间的间隔（以磅为单位）。

```csharp
public double DefaultTabStop { get; set; }
```

## 例子

显示如何为制表位位置设置自定义间隔。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 将制表位设置为每 72 点（1 英寸）出现一次。
builder.Document.DefaultTabStop = 72;

// 每个制表符将其后的文本捕捉到下一个最近的制表位位置。
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### 也可以看看

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
