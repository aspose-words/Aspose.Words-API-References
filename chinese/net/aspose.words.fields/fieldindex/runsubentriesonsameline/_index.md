---
title: FieldIndex.RunSubentriesOnSameLine
second_title: Aspose.Words for .NET API 参考
description: FieldIndex 财产. 获取或设置是否将子条目运行到与主条目相同的行中
type: docs
weight: 140
url: /zh/net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

获取或设置是否将子条目运行到与主条目相同的行中。

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

### 例子

显示如何使用 INDEX 字段中的子条目。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 INDEX 字段，它将为文档中找到的每个 XE 字段显示一个条目。
// 每个条目都会在左侧显示 XE 字段的 Text 属性值，
// 以及右侧包含 XE 字段的页码。
// INDEX 条目将收集所有在“Text”属性中具有匹配值的 XE 字段
// 进入一个条目，而不是为每个 XE 字段创建一个条目。
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// 具有 Text 属性的 XE 字段的值成为 INDEX 条目的标题。
// 如果此值包含由冒号分隔的两个字符串段（INDEX 条目将处理 :) 分隔符，
// 第一段是标题，第二段将成为副标题。
// INDEX 字段首先按字母顺序对条目进行分组，然后，如果有多个 XE 字段具有相同的
// 标题，INDEX 字段将根据这些标题的值进一步对它们进行分组。
// 可以有多个子分组层，取决于多少次
// XE 字段的 Text 属性是这样分段的。
 // 默认情况下，INDEX 字段条目组将为该组中的每个子标题创建一个新行。
// 我们可以将 RunSubentriesOnSameLine 标志设置为 true 以保持标题，
// 并将组的每个子标题放在一行中，这将使 INDEX 字段更紧凑。
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// 插入两个 XE 字段，每个都在一个新页面上，并且具有相同的标题，名为“标题 1”，
// INDEX 字段将用于对它们进行分组。
// 如果 RunSubentriesOnSameLine 为 false，则 INDEX 表将创建三行：
// 分组标题“标题 1”一行，每个子标题多一行。
// 如果 RunSubentriesOnSameLine 为 true，则 INDEX 表将创建一个单行
// 包含标题和每个子标题的条目。
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 1";

Assert.AreEqual(" XE  \"Heading 1:Subheading 1\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 2";

doc.UpdateFields();
doc.Save(ArtifactsDir + $"Field.INDEX.XE.Subheading.docx");
```

### 也可以看看

* class [FieldIndex](../)
* 命名空间 [Aspose.Words.Fields](../../fieldindex/)
* 部件 [Aspose.Words](../../../)


