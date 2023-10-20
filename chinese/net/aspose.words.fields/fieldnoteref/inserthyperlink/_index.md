---
title: FieldNoteRef.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: 用于 .NET 的 Aspose.Words
description: FieldNoteRef InsertHyperlink 财产. 获取或设置是否插入指向已添加书签的段落的超链接 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldnoteref/inserthyperlink/
---
## FieldNoteRef.InsertHyperlink property

获取或设置是否插入指向已添加书签的段落的超链接。

```csharp
public bool InsertHyperlink { get; set; }
```

## 例子

显示插入NOTEREF 字段并修改其外观。

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 创建带有脚注的书签，NOTEREF 字段将引用该脚注。
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // 此NOTEREF 字段将显示引用书签内脚注的编号。
    // 通过设置 InsertHyperlink 属性，我们可以通过按住 Ctrl 键并单击 Microsoft Word 中的字段来跳转到书签。
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // 当使用 \p 标志时，在脚注编号之后，该字段还显示书签相对于该字段的位置。
    // Bookmark1 位于该字段上方并包含脚注编号 1，因此更新时结果将为“上方 1”。
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bookmark2 位于该字段下方并包含脚注编号 2，因此该字段将显示“2 Below”。
    // \f 标志使数字 2 以与实际文本中脚注数字标签相同的格式出现。
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");
}

/// <summary>
/// 使用文档生成器插入具有指定属性的NOTEREF 字段。
/// </summary>
private static FieldNoteRef InsertFieldNoteRef(DocumentBuilder builder, string bookmarkName, bool insertHyperlink, bool insertRelativePosition, bool insertReferenceMark, string textBefore)
{
    builder.Write(textBefore);

    FieldNoteRef field = (FieldNoteRef)builder.InsertField(FieldType.FieldNoteRef, true);
    field.BookmarkName = bookmarkName;
    field.InsertHyperlink = insertHyperlink;
    field.InsertRelativePosition = insertRelativePosition;
    field.InsertReferenceMark = insertReferenceMark;
    builder.Writeln();

    return field;
}

/// <summary>
/// 使用文档生成器插入末尾带有脚注的命名书签。
/// </summary>
private static void InsertBookmarkWithFootnote(DocumentBuilder builder, string bookmarkName, string bookmarkText, string footnoteText)
{
    builder.StartBookmark(bookmarkName);
    builder.Write(bookmarkText);
    builder.InsertFootnote(FootnoteType.Footnote, footnoteText);
    builder.EndBookmark(bookmarkName);
    builder.Writeln();
}
```

### 也可以看看

* class [FieldNoteRef](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
