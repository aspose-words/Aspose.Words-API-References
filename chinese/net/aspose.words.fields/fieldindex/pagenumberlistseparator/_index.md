---
title: FieldIndex.PageNumberListSeparator
linktitle: PageNumberListSeparator
articleTitle: PageNumberListSeparator
second_title: 用于 .NET 的 Aspose.Words
description: FieldIndex PageNumberListSeparator 财产. 获取或设置用于分隔页码列表中两个页码的字符序列 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words.fields/fieldindex/pagenumberlistseparator/
---
## FieldIndex.PageNumberListSeparator property

获取或设置用于分隔页码列表中两个页码的字符序列。

```csharp
public string PageNumberListSeparator { get; set; }
```

## 例子

演示如何编辑 INDEX 字段中的页码分隔符。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 INDEX 字段，它将显示文档中找到的每个 XE 字段的条目。
// 每个条目都会在左侧显示XE字段的Text属性值，
// 以及右侧包含 XE 字段的页码。
// INDEX 条目会将 XE 字段与“Text”属性中的匹配值分组
// 进入一个条目，而不是为每个 XE 字段创建一个条目。
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// 如果我们的 INDEX 字段有一组 XE 字段的条目，
// 该条目将显示包含属于该组的 XE 字段的每个页面的编号。
// 我们可以设置自定义分隔符来自定义这些页码的外观。
index.PageNumberSeparator = ", on page(s) ";
index.PageNumberListSeparator = " & ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.GetFieldCode());
Assert.True(index.HasPageNumberSeparator);

// 在我们插入这些 XE 字段后，INDEX 字段将显示“第一个条目，第 2 & 3 & 4 页”。
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

Assert.AreEqual(" XE  \"First entry\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageNumberList.docx");
```

### 也可以看看

* class [FieldIndex](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
