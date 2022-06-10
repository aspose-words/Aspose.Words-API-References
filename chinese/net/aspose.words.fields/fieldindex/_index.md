---
title: FieldIndex
second_title: Aspose.Words for .NET API 参考
description: 实现 INDEX 字段
type: docs
weight: 1870
url: /zh/net/aspose.words.fields/fieldindex/
---
## FieldIndex class

实现 INDEX 字段。

```csharp
public class FieldIndex : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldIndex](fieldindex)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldindex/bookmarkname) { get; set; } | 获取或设置标记用于构建索引的文档部分的书签的名称。 |
| [CrossReferenceSeparator](../../aspose.words.fields/fieldindex/crossreferenceseparator) { get; set; } | 获取或设置用于分隔交叉引用和其他条目的字符序列。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end) { get; } | 获取表示字段结束的节点。 |
| [EntryType](../../aspose.words.fields/fieldindex/entrytype) { get; set; } | 获取或设置用于构建索引的索引条目类型。 |
| [Format](../../aspose.words.fields/field/format) { get; } | 获取[`FieldFormat`](../fieldformat)对象，该对象提供对字段格式的类型化访问。 |
| [HasPageNumberSeparator](../../aspose.words.fields/fieldindex/haspagenumberseparator) { get; } | 获取一个值，该值指示是否通过字段的代码覆盖页码分隔符。 |
| [HasSequenceName](../../aspose.words.fields/fieldindex/hassequencename) { get; } | 获取一个值，该值指示在构建字段结果时是否应使用序列。 |
| [Heading](../../aspose.words.fields/fieldindex/heading) { get; set; } | 获取或设置出现在任何给定字母的每组条目开头的标题。 |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | 获取或设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LanguageId](../../aspose.words.fields/fieldindex/languageid) { get; set; } | 获取或设置用于生成索引的语言 ID。 |
| [LetterRange](../../aspose.words.fields/fieldindex/letterrange) { get; set; } | 获取或设置限制索引的字母范围。 |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | 获取或设置字段的 LCID。 |
| [NumberOfColumns](../../aspose.words.fields/fieldindex/numberofcolumns) { get; set; } | 获取或设置建立索引时每页使用的列数。 |
| [PageNumberListSeparator](../../aspose.words.fields/fieldindex/pagenumberlistseparator) { get; set; } | 获取或设置用于分隔页码列表中两个页码的字符序列。 |
| [PageNumberSeparator](../../aspose.words.fields/fieldindex/pagenumberseparator) { get; set; } | 获取或设置用于分隔索引条目及其页码的字符序列。 |
| [PageRangeSeparator](../../aspose.words.fields/fieldindex/pagerangeseparator) { get; set; } | 获取或设置用于分隔页面范围的开始和结束的字符序列。 |
| [Result](../../aspose.words.fields/field/result) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [RunSubentriesOnSameLine](../../aspose.words.fields/fieldindex/runsubentriesonsameline) { get; set; } | 获取或设置是否将子条目运行到与主条目相同的行中。 |
| [Separator](../../aspose.words.fields/field/separator) { get; } | 获取表示字段分隔符的节点。可以为空。 |
| [SequenceName](../../aspose.words.fields/fieldindex/sequencename) { get; set; } | 获取或设置其编号包含在页码中的序列的名称。 |
| [SequenceSeparator](../../aspose.words.fields/fieldindex/sequenceseparator) { get; set; } | 获取或设置用于分隔序号和页码的字符序列。 |
| [Start](../../aspose.words.fields/field/start) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | 获取 Microsoft Word 字段类型。 |
| [UseYomi](../../aspose.words.fields/fieldindex/useyomi) { get; set; } | 获取或设置是否为索引条目启用读音文本。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包含子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove)() | 从文档中删除字段。在字段之后返回一个节点。如果字段的结尾是其父节点的最后一个子 ，则返回其父段落。如果该字段已被删除，则返回 **null** 。 |
| [Unlink](../../aspose.words.fields/field/unlink)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update)() | 执行字段更新。如果该字段已被更新，则抛出。 |
| [Update](../../aspose.words.fields/field/update)(bool) | 执行字段更新。如果该字段已被更新，则抛出。 |

### 评论

使用 XE 字段指定的索引条目构建索引，并将该索引插入到文件。

### 例子

展示如何创建一个 INDEX 字段，然后使用 XE 字段在其中填充条目。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 INDEX 字段，它将为文档中找到的每个 XE 字段显示一个条目。
// 每个条目都会在左侧显示 XE 字段的 Text 属性值，
// 以及右侧包含 XE 字段的页码。
// 如果 XE 字段的“Text”属性值相同，
// INDEX 字段会将它们分组到一个条目中。
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// 将此属性的值设置为“A”将按首字母对所有条目进行分组，
// 并将该字母以大写形式放在每个组的上方。
index.Heading = "A";

// 将 INDEX 字段创建的表设置为跨越 2 列。
index.NumberOfColumns = "2";

// 将所有起始字母超出“ac”字符范围的条目设置为被忽略。
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// 接下来的两个 XE 字段将显示在“A”标题下，
// 它们各自的文本样式也应用于它们的页码。
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

// INDEX 字段按字母顺序对所有条目进行排序，因此该条目将与其他两个一起显示在“A”下。
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// 这个条目不会出现，因为它以字母“D”开头，
// 它在 INDEX 字段的 LetterRange 属性定义的“ac”字符范围之外。
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

显示如何使用 XE 字段使用条目填充 INDEX 字段，并修改其外观。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 INDEX 字段，它将为文档中找到的每个 XE 字段显示一个条目。
// 每个条目都会在左侧显示 XE 字段的 Text 属性值，
// 以及右侧包含 XE 字段的页码。
// 如果 XE 字段的“Text”属性值相同，
// INDEX 字段会将它们分组到一个条目中。
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// 将此属性的值设置为“A”将按首字母对所有条目进行分组，
// 并将该字母以大写形式放在每个组的上方。
index.Heading = "A";

// 将 INDEX 字段创建的表设置为跨越 2 列。
index.NumberOfColumns = "2";

// 将所有起始字母超出“ac”字符范围的条目设置为被忽略。
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// 接下来的两个 XE 字段将显示在“A”标题下，
// 它们各自的文本样式也应用于它们的页码。
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

// INDEX 字段按字母顺序对所有条目进行排序，因此该条目将与其他两个一起显示在“A”下。
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// 这个条目不会出现，因为它以字母“D”开头，
// 它在 INDEX 字段的 LetterRange 属性定义的“ac”字符范围之外。
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### 也可以看看

* class [Field](../field)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
