---
title: FieldIndex.RunSubentriesOnSameLine
linktitle: RunSubentriesOnSameLine
articleTitle: RunSubentriesOnSameLine
second_title: Aspose.Words for .NET
description: 发现 FieldIndex RunSubentriesOnSameLine 属性，以便轻松管理与主条目内联的子条目，从而简化数据组织。
type: docs
weight: 140
url: /zh/net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

获取或设置是否将子条目运行到与主条目相同的行。

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

## 例子

展示如何使用 INDEX 字段中的子条目。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 INDEX 字段，它将显示文档中找到的每个 XE 字段的条目。
// 每个条目将在左侧显示 XE 字段的 Text 属性值，
// 以及右侧包含 XE 字段的页面的编号。
// INDEX 条目将收集“Text”属性中具有匹配值的所有 XE 字段
// 合并到一个条目中，而不是为每个 XE 字段创建一个条目。
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// 具有 Text 属性的 XE 字段，其值成为 INDEX 条目的标题。
// 如果此值包含两个由冒号分隔的字符串段（INDEX 条目将处理 :) 分隔符，
// 第一部分是标题，第二部分将成为副标题。
// INDEX 字段首先按字母顺序对条目进行分组，然后，如果有多个 XE 字段具有相同的
// 标题，INDEX 字段将根据这些标题的值进一步对它们进行分组。
// 可以有多个子分组层，取决于
// XE 字段的文本属性像这样分段。
// 默认情况下，INDEX 字段条目组将为该组内的每个子标题创建一个新行。
// 我们可以将 RunSubentriesOnSameLine 标志设置为 true 以保持标题，
// 并将组的每个子标题放在一行上，这将使 INDEX 字段更加紧凑。
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// 插入两个 XE 字段，每个字段位于一个新页面上，并且具有相同的标题，名为“标题 1”，
// INDEX 字段将使用其对它们进行分组。
// 如果 RunSubentriesOnSameLine 为 false，则 INDEX 表将创建三行：
// 一行用于分组标题“标题 1”，另外一行用于每个子标题。
// 如果 RunSubentriesOnSameLine 为真，则 INDEX 表将创建一行
// 包含标题和每个副标题的条目。
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 1";

Assert.AreEqual(" XE  \"Heading 1:Subheading 1\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 2";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + $"Field.INDEX.XE.Subheading.docx");
```

### 也可以看看

* class [FieldIndex](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
