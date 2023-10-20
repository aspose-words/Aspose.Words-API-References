---
title: RevisionColor Enum
linktitle: RevisionColor
articleTitle: RevisionColor
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Layout.RevisionColor 枚举. 允许指定文档修订的颜色 在 C#.
type: docs
weight: 3380
url: /zh/net/aspose.words.layout/revisioncolor/
---
## RevisionColor enumeration

允许指定文档修订的颜色。

```csharp
public enum RevisionColor
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Auto | `0` | 默认值。 |
| Black | `1` | 代表 000000 颜色。 |
| Blue | `2` | 代表 2e97d3 颜色。 |
| BrightGreen | `3` | 代表 84a35b 颜色。 |
| ClassicBlue | `4` | 代表 0000ff 颜色。 |
| ClassicRed | `5` | 代表 ff0000 颜色。 |
| DarkBlue | `6` | 代表 376e96 颜色。 |
| DarkRed | `7` | 代表 881824 种颜色。 |
| DarkYellow | `8` | 代表 e09a2b 颜色。 |
| Gray25 | `9` | 代表 a0a3a9 颜色。 |
| Gray50 | `10` | 代表 50565e 颜色。 |
| Green | `11` | 代表 2c6234 颜色。 |
| Pink | `12` | 代表 ce338f 颜色。 |
| Red | `13` | 代表 b5082e 颜色。 |
| Teal | `14` | 代表 1b9cab 颜色。 |
| Turquoise | `15` | 代表 3eafc2 颜色。 |
| Violet | `16` | 代表 633277 种颜色。 |
| White | `17` | 代表 ffffff 颜色。 |
| Yellow | `18` | 代表 fad272 颜色。 |
| NoHighlight | `19` | 没有使用颜色来突出显示修订版本更改。 |
| ByAuthor | `20` | 每个作者的修订都会收到自己的颜色，用于从一组预定义的高对比度颜色中突出显示。 |

## 例子

演示如何更改渲染输出文档中修订的外观。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个修订版本，然后将所有修订版本的颜色更改为绿色。
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// 删除出现在每条修改行左侧的栏。
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### 也可以看看

* 命名空间 [Aspose.Words.Layout](../../aspose.words.layout/)
* 部件 [Aspose.Words](../../)
