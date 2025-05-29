---
title: FieldXE.IsItalic
linktitle: IsItalic
articleTitle: IsItalic
second_title: Aspose.Words for .NET
description: 了解 FieldXE 的 IsItalic 属性如何通过轻松将斜体格式应用于页码以获得精美的外观来增强文档的样式。
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldxe/isitalic/
---
## FieldXE.IsItalic property

获取或设置是否对条目的页码应用斜体格式。

```csharp
public bool IsItalic { get; set; }
```

## 例子

展示如何使用 XE 字段填充 INDEX 字段，以及如何修改其外观。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 INDEX 字段，它将显示文档中找到的每个 XE 字段的条目。
// 每个条目将在左侧显示 XE 字段的 Text 属性值，
// 以及右侧包含 XE 字段的页面的编号。
// 如果 XE 字段的“Text”属性具有相同的值，
// INDEX 字段会将它们分组为一个条目。
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// 将此属性的值设置为“A”将按首字母对所有条目进行分组，
// 并将大写字母放在每个组上方。
index.Heading = "A";

// 设置由INDEX字段创建的表跨越2列。
index.NumberOfColumns = "2";

// 设置省略任何以“ac”字符范围之外的字母开头的条目。
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// 接下来的两个 XE 字段将显示在“A”标题下，
// 各自的文本样式也应用于其页码。
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// 接下来的两个 XE 字段都将位于 INDEX 字段目录中的“B”和“C”标题下。
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// INDEX 字段按字母顺序对所有条目进行排序，因此该条目将与其他两个条目一起显示在“A”下。
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// 该条目不会出现，因为它以字母“D”开头，
// 这超出了 INDEX 字段的 LetterRange 属性定义的“ac”字符范围。
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### 也可以看看

* class [FieldXE](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
