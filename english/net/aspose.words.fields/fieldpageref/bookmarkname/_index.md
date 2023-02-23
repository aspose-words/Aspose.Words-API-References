---
title: FieldPageRef.BookmarkName
linktitle: BookmarkName
second_title: Aspose.Words for .NET API Reference
description: FieldPageRef property. Gets or sets the name of the bookmark in C#.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldpageref/bookmarkname/
---
## FieldPageRef.BookmarkName property

Gets or sets the name of the bookmark.

```csharp
public string BookmarkName { get; set; }
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
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h", 
        InsertFieldPageRef(builder, "MyBookmark3", true, false, "Hyperlink to Bookmark3, on page: ").GetFieldCode());

    // We can use the \p flag to get the PAGEREF field to display
    // the bookmark's position relative to the position of the field.
    // Bookmark1 is on the same page and above this field, so this field's displayed result will be "above".
    Assert.AreEqual(" PAGEREF  MyBookmark1 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark1", true, true, "Bookmark1 is ").GetFieldCode());

    // Bookmark2 will be on the same page and below this field, so this field's displayed result will be "below".
    Assert.AreEqual(" PAGEREF  MyBookmark2 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark2", true, true, "Bookmark2 is ").GetFieldCode());

    // Bookmark3 will be on a different page, so the field will display "on page 2".
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark3", true, true, "Bookmark3 is ").GetFieldCode());

    InsertAndNameBookmark(builder, "MyBookmark2");
    builder.InsertBreak(BreakType.PageBreak);
    InsertAndNameBookmark(builder, "MyBookmark3");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.PAGEREF.docx");

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
* namespace [Aspose.Words.Fields](../../fieldpageref/)
* assembly [Aspose.Words](../../../)
