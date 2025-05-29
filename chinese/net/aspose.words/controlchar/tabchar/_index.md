---
title: ControlChar.TabChar
linktitle: TabChar
articleTitle: TabChar
second_title: Aspose.Words for .NET
description: 使用 ControlChar 轻松掌握 TabChar 字段，实现无缝数据管理。立即使用多功能制表符（char9 或 t）提升效率！
type: docs
weight: 280
url: /zh/net/aspose.words/controlchar/tabchar/
---
## ControlChar.TabChar field

制表符：(char)9 或 "\t".

```csharp
public const char TabChar;
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
