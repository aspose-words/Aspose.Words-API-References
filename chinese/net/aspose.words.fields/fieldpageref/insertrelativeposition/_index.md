---
title: FieldPageRef.InsertRelativePosition
linktitle: InsertRelativePosition
articleTitle: InsertRelativePosition
second_title: 用于 .NET 的 Aspose.Words
description: FieldPageRef InsertRelativePosition 财产. 获取或设置是否插入书签段落的相对位置 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldpageref/insertrelativeposition/
---
## FieldPageRef.InsertRelativePosition property

获取或设置是否插入书签段落的相对位置。

```csharp
public bool InsertRelativePosition { get; set; }
```

## 例子

显示插入 PAGEREF 字段以显示书签的相对位置。

```csharp
public void FieldPageRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);            

    InsertAndNameBookmark(builder, "MyBookmark1");

    // 插入一个 PAGEREF 字段，显示书签所在的页面。
    // 设置 InsertHyperlink 标志以使该字段也充当书签的可点击链接。
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h", 
        InsertFieldPageRef(builder, "MyBookmark3", true, false, "Hyperlink to Bookmark3, on page: ").GetFieldCode());

    // 我们可以使用 \p 标志来获取要显示的 PAGEREF 字段
    // 书签相对于字段位置的位置。
    // Bookmark1 位于同一页且位于该字段上方，因此该字段的显示结果将为“上方”。
    Assert.AreEqual(" PAGEREF  MyBookmark1 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark1", true, true, "Bookmark1 is ").GetFieldCode());

    // Bookmark2 将位于同一页并位于该字段下方，因此该字段的显示结果将为“下方”。
    Assert.AreEqual(" PAGEREF  MyBookmark2 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark2", true, true, "Bookmark2 is ").GetFieldCode());

    // Bookmark3 将位于不同的页面上，因此该字段将显示“在第 2 页上”。
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark3", true, true, "Bookmark3 is ").GetFieldCode());

    InsertAndNameBookmark(builder, "MyBookmark2");
    builder.InsertBreak(BreakType.PageBreak);
    InsertAndNameBookmark(builder, "MyBookmark3");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.PAGEREF.docx");
}

/// <summary>
/// 使用文档生成器插入 PAGEREF 字段并设置其属性。
/// </summary>
private static FieldPageRef InsertFieldPageRef(DocumentBuilder builder, string bookmarkName, bool insertHyperlink, bool insertRelativePosition, string textBefore)
{
    builder.Write(textBefore);

    FieldPageRef field = (FieldPageRef)builder.InsertField(FieldType.FieldPageRef, true);
    field.BookmarkName = bookmarkName;
    field.InsertHyperlink = insertHyperlink;
    field.InsertRelativePosition = insertRelativePosition;
    builder.Writeln();

    return field;
}

/// <summary>
/// 使用文档生成器插入命名书签。
/// </summary>
private static void InsertAndNameBookmark(DocumentBuilder builder, string bookmarkName)
{
    builder.StartBookmark(bookmarkName);
    builder.Writeln($"Contents of bookmark \"{bookmarkName}\".");
    builder.EndBookmark(bookmarkName);
}
```

### 也可以看看

* class [FieldPageRef](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
