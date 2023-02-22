---
title: FieldNoteRef.InsertHyperlink
second_title: Aspose.Words für .NET-API-Referenz
description: FieldNoteRef eigendom. Ruft ab oder legt fest ob ein Hyperlink zum mit Lesezeichen versehenen Absatz eingefügt werden soll.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldnoteref/inserthyperlink/
---
## FieldNoteRef.InsertHyperlink property

Ruft ab oder legt fest, ob ein Hyperlink zum mit Lesezeichen versehenen Absatz eingefügt werden soll.

```csharp
public bool InsertHyperlink { get; set; }
```

### Beispiele

Zeigt an, um NOTEREF-Felder einzufügen und ihr Aussehen zu ändern.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Erstellen Sie ein Lesezeichen mit einer Fußnote, auf die das Feld NOTEREF verweist.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // Dieses NOTEREF-Feld zeigt die Nummer der Fußnote innerhalb des referenzierten Lesezeichens an.
    // Wenn Sie die InsertHyperlink-Eigenschaft setzen, können wir zum Lesezeichen springen, indem Sie bei gedrückter Strg-Taste auf das Feld in Microsoft Word klicken.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // Bei Verwendung des \p-Flags zeigt das Feld nach der Fußnotennummer auch die Position des Lesezeichens relativ zum Feld an.
    // Lesezeichen1 befindet sich über diesem Feld und enthält die Fußnote Nummer 1, daher ist das Ergebnis bei der Aktualisierung "1 darüber".
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Lesezeichen2 befindet sich unter diesem Feld und enthält die Fußnote Nummer 2, sodass das Feld "2 unten" anzeigt.
    // Das \f-Flag lässt die Zahl 2 im gleichen Format wie die Fußnotennummer im eigentlichen Text erscheinen.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");

/// <summary>
/// Verwendet einen Document Builder, um ein NOTEREF-Feld mit angegebenen Eigenschaften einzufügen.
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
/// Verwendet einen Document Builder, um ein benanntes Lesezeichen mit einer Fußnote am Ende einzufügen.
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

### Siehe auch

* class [FieldNoteRef](../)
* namensraum [Aspose.Words.Fields](../../fieldnoteref/)
* Montage [Aspose.Words](../../../)


