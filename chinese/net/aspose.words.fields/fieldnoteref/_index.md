---
title: FieldNoteRef Class
linktitle: FieldNoteRef
articleTitle: FieldNoteRef
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fields.FieldNoteRef 班级. 实现NOTEREF 字段 在 C#.
type: docs
weight: 2200
url: /zh/net/aspose.words.fields/fieldnoteref/
---
## FieldNoteRef class

实现NOTEREF 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldNoteRef : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldNoteRef](fieldnoteref/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldnoteref/bookmarkname/) { get; set; } | 获取或设置书签的名称。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示的字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取表示字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式的类型化访问的对象。 |
| [InsertHyperlink](../../aspose.words.fields/fieldnoteref/inserthyperlink/) { get; set; } | 获取或设置是否插入指向已添加书签的段落的超链接。 |
| [InsertReferenceMark](../../aspose.words.fields/fieldnoteref/insertreferencemark/) { get; set; } | 插入与脚注参考 或尾注参考样式具有相同字符格式的引用标记。 |
| [InsertRelativePosition](../../aspose.words.fields/fieldnoteref/insertrelativeposition/) { get; set; } | 获取或设置是否插入书签段落的相对位置。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结束之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可`无效的`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中删除该字段。返回字段后面的节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果该字段已被更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果该字段已被更新，则抛出异常。 |

## 评论

插入由指定书签标记的脚注或尾注的标记。

## 例子

展示如何将脚注与NOTEREF字段交叉引用。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("CrossReference: ");

FieldNoteRef field = (FieldNoteRef)builder.InsertField(FieldType.FieldNoteRef, false); // <--- 不更新字段
field.BookmarkName = "CrossRefBookmark";
field.InsertHyperlink = true;
field.InsertReferenceMark = true;
field.InsertRelativePosition = false;
builder.Writeln();

builder.StartBookmark("CrossRefBookmark");
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Cross referenced footnote.");
builder.EndBookmark("CrossRefBookmark");
builder.Writeln();            

doc.UpdateFields();           

// 此字段仅适用于旧版本的 Microsoft Word。
doc.Save(ArtifactsDir + "Field.NOTEREF.doc");
```

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

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
