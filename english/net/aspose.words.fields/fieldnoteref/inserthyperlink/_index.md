---
title: FieldNoteRef.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words for .NET
description: Discover the FieldNoteRef InsertHyperlink property, easily manage hyperlink insertion for bookmarked paragraphs to enhance your document’s interactivity.
type: docs
weight: 30
url: /net/aspose.words.fields/fieldnoteref/inserthyperlink/
---
## FieldNoteRef.InsertHyperlink property

Gets or sets whether to insert a hyperlink to the bookmarked paragraph.

```csharp
public bool InsertHyperlink { get; set; }
```

## Examples

Shows to insert NOTEREF fields, and modify their appearance.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Create a bookmark with a footnote that the NOTEREF field will reference.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // This NOTEREF field will display the number of the footnote inside the referenced bookmark.
    // Setting the InsertHyperlink property lets us jump to the bookmark by Ctrl + clicking the field in Microsoft Word.
    Assert.That(InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode(), Is.EqualTo(" NOTEREF  MyBookmark2 \\h"));

    // When using the \p flag, after the footnote number, the field also displays the bookmark's position relative to the field.
    // Bookmark1 is above this field and contains footnote number 1, so the result will be "1 above" on update.
    Assert.That(InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode(), Is.EqualTo(" NOTEREF  MyBookmark1 \\h \\p"));

    // Bookmark2 is below this field and contains footnote number 2, so the field will display "2 below".
    // The \f flag makes the number 2 appear in the same format as the footnote number label in the actual text.
    Assert.That(InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode(), Is.EqualTo(" NOTEREF  MyBookmark2 \\h \\p \\f"));

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");
}

/// <summary>
/// Uses a document builder to insert a NOTEREF field with specified properties.
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
/// Uses a document builder to insert a named bookmark with a footnote at the end.
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

### See Also

* class [FieldNoteRef](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
