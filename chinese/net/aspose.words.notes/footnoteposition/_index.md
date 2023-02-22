---
title: Enum FootnotePosition
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Notes.FootnotePosition 枚举. 定义脚注位置
type: docs
weight: 4050
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
| BottomOfPage | `1` | 在每页底部输出脚注。 |
| BeneathText | `2` | 脚注输出在每页文本下方。 |

### 例子

显示如何选择文档收集和显示脚注的不同位置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 脚注是一种将引用或旁注附加到文本的方法
// 这不会干扰主体文本的流动。  
// 插入脚注会添加一个小的上标参考符号
// 在我们插入脚注的主体文本处。
// 每个脚注还在页面底部创建一个条目，由一个符号组成
// 与正文中的引用符号匹配。
// 我们传递给文档构建器的“InsertFootnote”方法的参考文本。
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// 我们可以使用“Position”属性来确定文档将放置其所有脚注的位置。
// 如果我们将“Position”属性的值设置为“FootnotePosition.BottomOfPage”，
// 每个脚注都将显示在包含其引用标记的页面底部。这是默认值。
// 如果我们将“Position”属性的值设置为“FootnotePosition.BeneathText”，
// 每个脚注都将显示在包含其引用标记的页面文本的末尾。
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### 也可以看看

* class [FootnoteOptions](../footnoteoptions/)
* 命名空间 [Aspose.Words.Notes](../../aspose.words.notes/)
* 部件 [Aspose.Words](../../)


