---
title: FieldPageRef.InsertRelativePosition
linktitle: InsertRelativePosition
articleTitle: InsertRelativePosition
second_title: Aspose.Words for .NET
description: Discover how the InsertRelativePosition property of FieldPageRef enhances document navigation by managing bookmarked paragraph positions effectively.
type: docs
weight: 40
url: /net/aspose.words.fields/fieldpageref/insertrelativeposition/
---
## FieldPageRef.InsertRelativePosition property

Gets or sets whether to insert a relative position of the bookmarked paragraph.

```csharp
public bool InsertRelativePosition { get; set; }
```

## Examples

Shows to insert PAGEREF fields to display the relative location of bookmarks.

```csharp
public void FieldPageRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    InsertAndNameBookmark(builder, "MyBookmark1");

    // Insert a PAGEREF field that displays what page a bookmark is on.
    // Set the InsertHyperlink flag to make the field also function as a clickable link to the bookmark.
    Assert.That(InsertFieldPageRef(builder, "MyBookmark3", true, false, "Hyperlink to Bookmark3, on page: ").GetFieldCode(), Is.EqualTo(" PAGEREF  MyBookmark3 \\h"));

    // We can use the \p flag to get the PAGEREF field to display
    // the bookmark's position relative to the position of the field.
    // Bookmark1 is on the same page and above this field, so this field's displayed result will be "above".
    Assert.That(InsertFieldPageRef(builder, "MyBookmark1", true, true, "Bookmark1 is ").GetFieldCode(), Is.EqualTo(" PAGEREF  MyBookmark1 \\h \\p"));

    // Bookmark2 will be on the same page and below this field, so this field's displayed result will be "below".
    Assert.That(InsertFieldPageRef(builder, "MyBookmark2", true, true, "Bookmark2 is ").GetFieldCode(), Is.EqualTo(" PAGEREF  MyBookmark2 \\h \\p"));

    // Bookmark3 will be on a different page, so the field will display "on page 2".
    Assert.That(InsertFieldPageRef(builder, "MyBookmark3", true, true, "Bookmark3 is ").GetFieldCode(), Is.EqualTo(" PAGEREF  MyBookmark3 \\h \\p"));

    InsertAndNameBookmark(builder, "MyBookmark2");
    builder.InsertBreak(BreakType.PageBreak);
    InsertAndNameBookmark(builder, "MyBookmark3");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.PAGEREF.docx");
}

/// <summary>
/// Uses a document builder to insert a PAGEREF field and sets its properties.
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
/// Uses a document builder to insert a named bookmark.
/// </summary>
private static void InsertAndNameBookmark(DocumentBuilder builder, string bookmarkName)
{
    builder.StartBookmark(bookmarkName);
    builder.Writeln($"Contents of bookmark \"{bookmarkName}\".");
    builder.EndBookmark(bookmarkName);
}
```

### See Also

* class [FieldPageRef](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
