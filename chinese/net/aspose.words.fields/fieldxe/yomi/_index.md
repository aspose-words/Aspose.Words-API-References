---
title: FieldXE.Yomi
linktitle: Yomi
articleTitle: Yomi
second_title: Aspose.Words for .NET
description: 使用 FieldXE Yomi 属性优化您的索引条目，使用第一个语音字符实现高效排序，从而增强数据组织。
type: docs
weight: 80
url: /zh/net/aspose.words.fields/fieldxe/yomi/
---
## FieldXE.Yomi property

获取或设置索引条目的读音（用于排序索引的第一个语音字符）

```csharp
public string Yomi { get; set; }
```

## 例子

显示如何按语音对 INDEX 字段条目进行排序。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 INDEX 字段，它将显示文档中找到的每个 XE 字段的条目。
// 每个条目将在左侧显示 XE 字段的 Text 属性值，
// 以及右侧包含 XE 字段的页面的编号。
// INDEX 条目将收集“Text”属性中具有匹配值的所有 XE 字段
// 合并到一个条目中，而不是为每个 XE 字段创建一个条目。
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// INDEX 表自动按照其 Text 属性的值按字母顺序对其条目进行排序。
// 设置 INDEX 表以使用平假名按语音对条目进行排序。
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// 插入 4 个 XE 字段，它们将显示为 INDEX 字段目录中的条目。
// “Text” 属性可能包含汉字的拼写，其发音可能有歧义，
// 而单词的“Yomi”版本将准确拼写其使用平假名时的发音。
// 如果我们设置 INDEX 字段使用 Yomi，它将对这些条目进行排序
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

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Yomi.docx");
```

### 也可以看看

* class [FieldXE](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
