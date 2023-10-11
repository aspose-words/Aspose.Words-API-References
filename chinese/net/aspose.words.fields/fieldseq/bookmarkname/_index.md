---
title: FieldSeq.BookmarkName
second_title: Aspose.Words for .NET API 参考
description: FieldSeq 财产. 获取或设置引用文档中其他位置而不是当前位置的项目的书签名称
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldseq/bookmarkname/
---
## FieldSeq.BookmarkName property

获取或设置引用文档中其他位置而不是当前位置的项目的书签名称。

```csharp
public string BookmarkName { get; set; }
```

### 例子

展示如何组合目录和序列字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// TOC 字段可以在其目录中为文档中找到的每个 SEQ 字段创建一个条目。
// 每个条目包含包含 SEQ 字段的段落，
// 以及该字段出现的页码。
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// 配置此 TOC 字段以具有值为“MySequence”的 SequenceIdentifier 属性。
fieldToc.TableOfFiguresLabel = "MySequence";

// 配置此 TOC 字段以仅选取书签范围内的 SEQ 字段
// 命名为“TOCBookmark”。
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// SEQ 字段显示在每个 SEQ 字段处递增的计数。
// 这些字段还为每个唯一的命名序列维护单独的计数
// 由 SEQ 字段的“SequenceIdentifier”属性标识。
// 插入一个 SEQ 字段，该字段具有与 TOC 匹配的序列标识符
// TableOfFiguresLabel 属性。该字段不会在目录中创建条目，因为它位于外部
// 由“BookmarkName”指定的书签边界。
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// 此 SEQ 字段的序列与 TOC 的“TableOfFiguresLabel”属性匹配，并且在书签的范围内。
// 包含此字段的段落将作为条目显示在目录中。
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// 此 SEQ 字段的序列与 TOC 的“TableOfFiguresLabel”属性不匹配，
// 并且在书签的范围内。它的段落不会作为条目出现在目录中。
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// 此 SEQ 字段的序列与 TOC 的“TableOfFiguresLabel”属性匹配，并且在书签的范围内。
// 该字段还引用另一个书签。该书签的内容将出现在该 SEQ 字段的 TOC 条目中。
// SEQ 字段本身不会显示该书签的内容。
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// 创建一个书签，其中的内容将由于上述 SEQ 字段引用而显示在 TOC 条目中。
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
```

### 也可以看看

* class [FieldSeq](../)
* 命名空间 [Aspose.Words.Fields](../../fieldseq/)
* 部件 [Aspose.Words](../../../)


