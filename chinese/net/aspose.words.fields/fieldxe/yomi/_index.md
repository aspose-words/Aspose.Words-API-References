---
title: FieldXE.Yomi
linktitle: Yomi
articleTitle: Yomi
second_title: 用于 .NET 的 Aspose.Words
description: FieldXE Yomi 财产. 获取或设置索引条目的 yomi排序索引的第一个音标 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words.fields/fieldxe/yomi/
---
## FieldXE.Yomi property

获取或设置索引条目的 yomi（排序索引的第一个音标）

```csharp
public string Yomi { get; set; }
```

## 例子

显示如何按语音对 INDEX 字段条目进行排序。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 INDEX 字段，它将为文档中找到的每个 XE 字段显示一个条目。
// 每个条目都会在左侧显示 XE 字段的 Text 属性值，
// 以及右侧包含 XE 字段的页码。
// INDEX 条目将收集所有在“Text”属性中具有匹配值的 XE 字段
// 进入一个条目，而不是为每个 XE 字段创建一个条目。
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// INDEX 表自动按其文本属性的值按字母顺序对其条目进行排序。
// 将 INDEX 表设置为使用平假名对条目进行拼音排序。
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// 插入 4 个 XE 字段，它们将在 INDEX 字段的目录中显示为条目。
// “Text”属性可能包含一个单词的汉字拼写，其发音可能有歧义，
// 而单词的“Yomi”版本将使用平假名准确拼写它的发音。
// 如果我们将 INDEX 字段设置为使用 Yomi，它将对这些条目进行排序
// 通过它们的 Yomi 属性的值，而不是它们的 Text 值。
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛子";
indexEntry.Yomi = "あ";

Assert.AreEqual(" XE  愛子 \\y あ", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "明美";
indexEntry.Yomi = "あ";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "恵美";
indexEntry.Yomi = "え";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛美";
indexEntry.Yomi = "え";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Yomi.docx");
```

### 也可以看看

* class [FieldXE](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
