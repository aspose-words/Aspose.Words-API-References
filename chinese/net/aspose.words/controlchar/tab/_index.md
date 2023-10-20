---
title: ControlChar.Tab
linktitle: Tab
articleTitle: Tab
second_title: 用于 .NET 的 Aspose.Words
description: ControlChar Tab 场地. 制表符x0009或t 在 C#.
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

* class [ControlChar](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
