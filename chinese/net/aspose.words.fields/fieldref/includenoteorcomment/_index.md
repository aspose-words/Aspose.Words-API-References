---
title: FieldRef.IncludeNoteOrComment
linktitle: IncludeNoteOrComment
articleTitle: IncludeNoteOrComment
second_title: Aspose.Words for .NET
description: 发现 FieldRef IncludeNoteOrComment 属性可以轻松管理脚注和尾注编号，并通过无缝注释增强您的文档。
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldref/includenoteorcomment/
---
## FieldRef.IncludeNoteOrComment property

获取或设置是否增加书签标记的脚注、尾注和注释编号，并插入相应的脚注、尾注和注释文本。

```csharp
public bool IncludeNoteOrComment { get; set; }
```

## 例子

显示如何将 REF 字段插入到参考书签。

```csharp
public void FieldRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #1");
    builder.Write("Text that will appear in REF field");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #2");
    builder.EndBookmark("MyBookmark");
    builder.MoveToDocumentStart();

    // 我们将应用自定义列表格式，其中尖括号的数量表示我们当前所处的列表级别。
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // 插入一个 REF 字段，该字段将包含书签中的文本，充当超链接，并克隆书签的脚注。
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // 插入一个 REF 字段，并显示引用的书签是在其上方还是下方。
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // 显示文档中书签的列表编号。
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // 显示书签的列表编号，但省略非分隔符，例如尖括号。
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // 向下移动一个列表级别。
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // 显示书签的列表编号以及其上所有列表级别的编号。
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // 显示此 REF 字段与其引用的书签之间的列表级别编号。
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // 在文档末尾，书签将作为列表项显示在此处。
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");
}

/// <summary>
/// 获取文档构建器插入 REF 字段，用它引用书签，并在其前后添加文本。
/// </summary>
private static FieldRef InsertFieldRef(DocumentBuilder builder, string bookmarkName, string textBefore, string textAfter)
{
    builder.Write(textBefore);
    FieldRef field = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    field.BookmarkName = bookmarkName;
    builder.Write(textAfter);
    return field;
}
```

### 也可以看看

* class [FieldRef](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
