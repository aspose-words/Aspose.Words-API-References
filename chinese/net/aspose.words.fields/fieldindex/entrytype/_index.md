---
title: FieldIndex.EntryType
linktitle: EntryType
articleTitle: EntryType
second_title: Aspose.Words for .NET
description: 发现 FieldIndex EntryType 属性以有效管理索引条目类型，从而优化索引并增强搜索性能。
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldindex/entrytype/
---
## FieldIndex.EntryType property

获取或设置用于构建索引的索引条目类型。

```csharp
public string EntryType { get; set; }
```

## 例子

展示如何创建 INDEX 字段，然后使用 XE 字段填充条目。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 INDEX 字段，它将显示文档中找到的每个 XE 字段的条目。
// 每个条目将在左侧显示 XE 字段的 Text 属性值
// 以及右侧包含 XE 字段的页面。
// 如果 XE 字段的“Text”属性具有相同的值，
// INDEX 字段会将它们分组为一个条目。
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// 配置 INDEX 字段仅显示边界内的 XE 字段
// 名为“MainBookmark”的书签，其“EntryType”属性的值为“A”。
// 对于 INDEX 和 XE 字段，“EntryType”属性仅使用其字符串值的第一个字符。
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// 在新页面上，使用与值匹配的名称开始书签
// INDEX 字段的“BookmarkName”属性。
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// INDEX 字段将选取此条目，因为它位于书签内，
// 并且其条目类型也与 INDEX 字段的条目类型匹配。
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// 插入一个不会出现在 INDEX 中的 XE 字段，因为条目类型不匹配。
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// 结束书签并在之后插入 XE 字段。
// 与INDEX字段类型相同，但不会出现
// 因为它超出了书签的边界。
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

### 也可以看看

* class [FieldIndex](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
