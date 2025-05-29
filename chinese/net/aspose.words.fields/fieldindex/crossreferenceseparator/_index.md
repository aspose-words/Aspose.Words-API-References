---
title: FieldIndex.CrossReferenceSeparator
linktitle: CrossReferenceSeparator
articleTitle: CrossReferenceSeparator
second_title: Aspose.Words for .NET
description: 发现 FieldIndex CrossReferenceSeparator 属性，轻松管理字符序列，从而有效地分隔交叉引用和条目。
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldindex/crossreferenceseparator/
---
## FieldIndex.CrossReferenceSeparator property

获取或设置用于分隔交叉引用和其他条目的字符序列。

```csharp
public string CrossReferenceSeparator { get; set; }
```

## 例子

展示如何在 INDEX 字段中定义交叉引用。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 INDEX 字段，它将显示文档中找到的每个 XE 字段的条目。
// 每个条目将在左侧显示 XE 字段的 Text 属性值，
// 以及右侧包含 XE 字段的页面的编号。
// INDEX 条目将收集“Text”属性中具有匹配值的所有 XE 字段
// 合并到一个条目中，而不是为每个 XE 字段创建一个条目。
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// 我们可以配置一个 XE 字段来让其 INDEX 条目显示字符串而不是页码。
// 首先，对于用字符串替换页码的条目，
// 在 XE 字段的 Text 属性值和字符串之间指定自定义分隔符。
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// 插入一个 XE 字段，该字段创建一个常规 INDEX 条目，显示该字段的页码，
// 并且不调用 CrossReferenceSeparator 值。
// 此 XE 字段的条目将显示“Apple, 2”。
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// 在第 3 页插入另一个 XE 字段并为 PageNumberReplacement 属性设置一个值。
// 该值将显示出来，而不是该字段所在页码，
// 并且 INDEX 字段的 CrossReferenceSeparator 值将出现在其前面。
// 此 XE 字段的条目将显示“香蕉，参见：热带水果”。
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";
indexEntry.PageNumberReplacement = "Tropical fruit";

Assert.AreEqual(" XE  Banana \\t \"Tropical fruit\"", indexEntry.GetFieldCode());

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.CrossReferenceSeparator.docx");
```

### 也可以看看

* class [FieldIndex](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
