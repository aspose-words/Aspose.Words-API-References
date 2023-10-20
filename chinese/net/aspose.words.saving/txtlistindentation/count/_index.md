---
title: TxtListIndentation.Count
linktitle: Count
articleTitle: Count
second_title: 用于 .NET 的 Aspose.Words
description: TxtListIndentation Count 财产. 获取或设置多少Character用作每一级列表的缩进 默认值为 0这意味着没有缩进 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.saving/txtlistindentation/count/
---
## TxtListIndentation.Count property

获取或设置多少[`Character`](../character/)用作每一级列表的缩进。 默认值为 0，这意味着没有缩进。

```csharp
public int Count { get; set; }
```

## 例子

演示如何在将文档保存为纯文本时配置列表缩进。

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

// 设置“Character”属性来指定要使用的字符
// 用于模拟明文列表缩进的填充。
txtSaveOptions.ListIndentation.Character = ' ';

// 设置“Count”属性来指定次数
// 为每个列表缩进级别放置填充字符。
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");

Assert.AreEqual("1. Item 1\r\n" +
                "   a. Item 2\r\n" +
                "      i. Item 3\r\n", docText);
```

### 也可以看看

* class [TxtListIndentation](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
