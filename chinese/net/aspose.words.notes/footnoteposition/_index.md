---
title: FootnotePosition Enum
linktitle: FootnotePosition
articleTitle: FootnotePosition
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Notes.FootnotePosition 枚举，用于可自定义的脚注位置，增强文档格式和可读性。
type: docs
weight: 4980
url: /zh/net/aspose.words.notes/footnoteposition/
---
## FootnotePosition enumeration

定义脚注位置。

```csharp
public enum FootnotePosition
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| BottomOfPage | `1` | 脚注输出在每页的底部。 |
| BeneathText | `2` | 脚注输出在每页的文本下方。 |

## 例子

显示如何选择文档收集和显示其脚注的不同位置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 脚注是一种将参考或旁注附加到文本的方式
// 不会干扰正文的流程。
// 插入脚注会添加一个小上标引用符号
// 在正文中插入脚注。
// 每个脚注还会在页面底部创建一个条目，由一个符号组成
// 与正文中的参考符号相匹配。
// 我们传递给文档构建器的“InsertFootnote”方法的参考文本。
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// 我们可以使用“Position”属性来确定文档将所有脚注放置在何处。
// 如果我们将“Position”属性的值设置为“FootnotePosition.BottomOfPage”，
// 每个脚注都会显示在包含其引用标记的页面底部。这是默认值。
// 如果我们将“Position”属性的值设置为“FootnotePosition.BeneathText”，
// 每个脚注都会出现在包含其引用标记的页面文本的末尾。
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### 也可以看看

* class [FootnoteOptions](../footnoteoptions/)
* 命名空间 [Aspose.Words.Notes](../../aspose.words.notes/)
* 部件 [Aspose.Words](../../)
