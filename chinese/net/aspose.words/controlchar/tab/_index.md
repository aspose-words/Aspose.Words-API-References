---
title: ControlChar.Tab
linktitle: Tab
articleTitle: Tab
second_title: Aspose.Words for .NET
description: 发现 ControlChar Tab 字段，了解 Tab 字符 x0009 以实现高效的文本格式化和增强的数据管理。
type: docs
weight: 270
url: /zh/net/aspose.words/controlchar/tab/
---
## ControlChar.Tab field

制表符：“\x0009”或“\t”。

```csharp
public static readonly string Tab;
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

* class [ControlChar](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
