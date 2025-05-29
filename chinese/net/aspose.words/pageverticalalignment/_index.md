---
title: PageVerticalAlignment Enum
linktitle: PageVerticalAlignment
articleTitle: PageVerticalAlignment
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.PageVerticalAlignment 枚举，实现页面文本最佳对齐。通过精确的垂直对齐，增强文档布局！
type: docs
weight: 5100
url: /zh/net/aspose.words/pageverticalalignment/
---
## PageVerticalAlignment enumeration

指定每页文本的垂直对齐。

```csharp
public enum PageVerticalAlignment
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Bottom | `3` | 文本与页面底部对齐。 |
| Center | `1` | 文本与页面中间对齐。 |
| Justify | `2` | 文本展开以填满整个页面。 |
| Top | `0` | 文本与页面顶部对齐。 |

## 例子

展示如何将页面设置应用到文档的各个部分以及将其恢复为页面设置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 修改构建器当前部分的页面设置属性并添加文本。
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// 如果我们使用文档生成器开始一个新的部分，
// 它将继承构建器的当前页面设置属性。
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// 我们可以使用“ClearFormatting”方法将其页面设置属性恢复为默认值。
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### 也可以看看

* class [PageSetup](../pagesetup/)
* property [VerticalAlignment](../pagesetup/verticalalignment/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
