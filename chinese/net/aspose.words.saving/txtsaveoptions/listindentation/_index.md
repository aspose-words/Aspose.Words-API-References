---
title: TxtSaveOptions.ListIndentation
linktitle: ListIndentation
articleTitle: ListIndentation
second_title: Aspose.Words for .NET
description: 探索 TxtSaveOptions ListIndentation 属性，它可以自定义列表缩进，增强可读性。轻松控制字符和级别！
type: docs
weight: 30
url: /zh/net/aspose.words.saving/txtsaveoptions/listindentation/
---
## TxtSaveOptions.ListIndentation property

获得[`TxtListIndentation`](../../txtlistindentation/)指定列表级别缩进所用字符数和字符数的对象。 默认情况下，字符 '\0' 的计数为零，即不缩进。

```csharp
public TxtListIndentation ListIndentation { get; }
```

## 例子

展示如何在将文档保存为纯文本时配置列表缩进。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个具有三级缩进的列表。
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// 创建一个“TxtSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改我们将文档保存为纯文本的方式。
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// 设置“Character”属性来分配要使用的字符
// 用于模拟纯文本列表缩进的填充。
txtSaveOptions.ListIndentation.Character = ' ';

// 设置“Count”属性来指定次数
// 为每个列表缩进级别放置填充字符。
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");
string newLine= Environment.NewLine;

Assert.AreEqual($"1. Item 1{newLine}" +
                $"   a. Item 2{newLine}" +
                $"      i. Item 3{newLine}", docText);
```

### 也可以看看

* class [TxtListIndentation](../../txtlistindentation/)
* class [TxtSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
