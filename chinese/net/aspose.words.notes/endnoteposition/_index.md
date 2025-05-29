---
title: EndnotePosition Enum
linktitle: EndnotePosition
articleTitle: EndnotePosition
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words EndnotePosition 枚举，以精确控制文档中的尾注位置，增强您的文本格式化能力。
type: docs
weight: 4940
url: /zh/net/aspose.words.notes/endnoteposition/
---
## EndnotePosition enumeration

定义尾注位置。

```csharp
public enum EndnotePosition
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| EndOfSection | `0` | 尾注输出于章节末尾。 |
| EndOfDocument | `3` | 尾注输出在文档末尾。 |

## 例子

显示如何选择文档收集和显示其尾注的不同位置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 尾注是一种将参考或旁注附加到文本的方式
// 不会干扰正文的流程。
// 插入尾注会添加一个小上标引用符号
// 在主体文本中插入尾注。
// 每个尾注还会在文档末尾创建一个条目，由一个符号组成
// 与正文中的参考符号相匹配。
// 我们传递给文档构建器的“InsertEndnote”方法的参考文本。
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// 我们可以使用“Position”属性来确定文档将所有尾注放置在何处。
// 如果我们将“Position”属性的值设置为“EndnotePosition.EndOfDocument”，
// 每个脚注都会显示在文档末尾的集合中。这是默认值。
// 如果我们将“Position”属性的值设置为“EndnotePosition.EndOfSection”，
// 每个脚注都会出现在文本包含尾注引用标记的部分末尾的集合中。
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

### 也可以看看

* class [EndnoteOptions](../endnoteoptions/)
* 命名空间 [Aspose.Words.Notes](../../aspose.words.notes/)
* 部件 [Aspose.Words](../../)
