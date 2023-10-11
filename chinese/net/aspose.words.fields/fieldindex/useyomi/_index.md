---
title: FieldIndex.UseYomi
second_title: Aspose.Words for .NET API 参考
description: FieldIndex 财产. 获取或设置是否启用索引条目使用 yomi 文本
type: docs
weight: 170
url: /zh/net/aspose.words.fields/fieldindex/useyomi/
---
## FieldIndex.UseYomi property

获取或设置是否启用索引条目使用 yomi 文本。

```csharp
public bool UseYomi { get; set; }
```

### 例子

演示如何按语音对 INDEX 字段条目进行排序。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 INDEX 字段，它将显示文档中找到的每个 XE 字段的条目。
// 每个条目都会在左侧显示XE字段的Text属性值，
// 以及右侧包含 XE 字段的页码。
// INDEX 条目将收集“Text”属性中具有匹配值的所有 XE 字段
// 进入一个条目，而不是为每个 XE 字段创建一个条目。
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// INDEX 表自动根据其 Text 属性的值按字母顺序对其条目进行排序。
// 设置 INDEX 表以使用平假名按语音对条目进行排序。
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// 插入 4 个 XE 字段，这些字段将显示为 INDEX 字段的目录中的条目。
// “Text”属性可能包含一个单词的汉字拼写，其发音可能有歧义，
// 而该词的“Yomi”版本将准确拼写它使用平假名的发音。
// 如果我们将 INDEX 字段设置为使用 Yomi，它将对这些条目进行排序
// 通过其 Yomi 属性的值，而不是其 Text 值。
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

* class [FieldIndex](../)
* 命名空间 [Aspose.Words.Fields](../../fieldindex/)
* 部件 [Aspose.Words](../../../)


