---
title: Paragraph.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: 用于 .NET 的 Aspose.Words
description: Paragraph JoinRunsWithSameFormatting 方法. 连接段落中具有相同格式的运行 在 C#.
type: docs
weight: 280
url: /zh/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

连接段落中具有相同格式的运行。

```csharp
public int JoinRunsWithSameFormatting()
```

### 返回值

执行的连接数。什么时候**氮**相邻的运行被连接起来，它们算作**N-1**加入。

## 例子

展示如何通过合并多余的段落来简化段落。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在段落中插入四段文本。
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// 如果我们在 Microsoft Word 中打开此文档，该段落将看起来像一个无缝文本正文。
// 但是，它将由具有相同格式的四个单独的运行组成。像这样断断续续的段落
// 当我们在 Microsoft Word 中多次手动编辑一个段落的某些部分时，可能会出现这种情况。
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// 更改最后一次运行的样式以将其与前三个运行区分开。
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// 我们可以运行“JoinRunsWithSameFormatting”方法来优化文档的内容
// 通过将相似的运行合并为一个，减少它们的总数。
// 此方法还返回此方法合并的运行次数。
// 这两次合并是为了合并运行 #1、#2 和 #3，
// 同时省略 Run #4，因为它具有不兼容的样式。
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// 剩余的运行次数将等于原始计数
// 减去“JoinRunsWithSameFormatting”方法执行的运行合并次数。
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### 也可以看看

* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
