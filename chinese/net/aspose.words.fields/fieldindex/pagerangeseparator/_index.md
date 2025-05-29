---
title: FieldIndex.PageRangeSeparator
linktitle: PageRangeSeparator
articleTitle: PageRangeSeparator
second_title: Aspose.Words for .NET
description: 探索 FieldIndex 中的 PageRangeSeparator 属性。轻松自定义字符序列，实现无缝的页面范围格式化，提升文档的清晰度。
type: docs
weight: 130
url: /zh/net/aspose.words.fields/fieldindex/pagerangeseparator/
---
## FieldIndex.PageRangeSeparator property

获取或设置用于分隔页面范围的开始和结束的字符序列。

```csharp
public string PageRangeSeparator { get; set; }
```

## 例子

展示如何将书签的跨页指定为 INDEX 字段条目的页面范围。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个 INDEX 字段，它将显示文档中找到的每个 XE 字段的条目。
// 每个条目将在左侧显示 XE 字段的 Text 属性值，
// 以及右侧包含 XE 字段的页面的编号。
// INDEX 条目将收集“Text”属性中具有匹配值的所有 XE 字段
// 合并到一个条目中，而不是为每个 XE 字段创建一个条目。
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// 对于显示页面范围的 INDEX 条目，我们可以指定分隔符字符串
// 它将出现在第一页的页码和最后一页的页码之间。
index.PageNumberSeparator = ", on page(s) ";
index.PageRangeSeparator = " to ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "My entry";

// 如果 XE 字段使用 PageRangeBookmarkName 属性命名书签，
// 其 INDEX 条目将显示书签跨越的页面范围
// 而不是包含 XE 字段的页面的编号。
indexEntry.PageRangeBookmarkName = "MyBookmark";

Assert.AreEqual(" XE  \"My entry\" \\r MyBookmark", indexEntry.GetFieldCode());
Assert.AreEqual("MyBookmark", indexEntry.PageRangeBookmarkName);

// 插入从第 3 页开始到第 5 页结束的书签。
// 引用此书签的 XE 字段的 INDEX 条目将显示此页面范围。
// 在我们的表格中，INDEX 条目将显示“我的条目，在第 3 至 5 页”。
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MyBookmark");
builder.Write("Start of MyBookmark");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.Write("End of MyBookmark");
builder.EndBookmark("MyBookmark");

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageRangeBookmark.docx");
```

### 也可以看看

* class [FieldIndex](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
