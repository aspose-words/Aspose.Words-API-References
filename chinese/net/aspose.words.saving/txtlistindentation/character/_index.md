---
title: TxtListIndentation.Character
linktitle: Character
articleTitle: Character
second_title: Aspose.Words for .NET
description: 探索 TxtListIndentation 属性，使用您喜欢的字符自定义列表缩进。轻松提升可读性和视觉吸引力！
type: docs
weight: 20
url: /zh/net/aspose.words.saving/txtlistindentation/character/
---
## TxtListIndentation.Character property

获取或设置用于缩进列表级别的字符。 默认值为“\0”，表示没有缩进。

```csharp
public char Character { get; set; }
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

* class [TxtListIndentation](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
