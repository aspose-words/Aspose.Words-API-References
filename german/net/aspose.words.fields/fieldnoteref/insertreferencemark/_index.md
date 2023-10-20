---
title: FieldNoteRef.InsertReferenceMark
linktitle: InsertReferenceMark
articleTitle: InsertReferenceMark
second_title: Aspose.Words für .NET
description: FieldNoteRef InsertReferenceMark eigendom. Fügt die Referenzmarke mit derselben Zeichenformatierung wie der Fußnotenreferenz  oder Endnotenreferenzstil ein in C#.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldnoteref/insertreferencemark/
---
## FieldNoteRef.InsertReferenceMark property

Fügt die Referenzmarke mit derselben Zeichenformatierung wie der Fußnotenreferenz- - oder Endnotenreferenzstil ein.

```csharp
public bool InsertReferenceMark { get; set; }
```

## Beispiele

Zeigt das Einfügen von NOTEREF-Feldern und das Ändern ihres Erscheinungsbilds an.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Erstellen Sie ein Lesezeichen mit einer Fußnote, auf die das NOTEREF-Feld verweist.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // Dieses NOTEREF-Feld zeigt die Nummer der Fußnote innerhalb des referenzierten Lesezeichens an.
    // Durch Festlegen der Eigenschaft „InsertHyperlink“ können wir zum Lesezeichen springen, indem wir in Microsoft Word bei gedrückter Strg-Taste auf das Feld klicken.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // Bei Verwendung des \p-Flags zeigt das Feld nach der Fußnotennummer auch die Position des Lesezeichens relativ zum Feld an.
    // Lesezeichen1 befindet sich über diesem Feld und enthält die Fußnote Nummer 1, sodass das Ergebnis bei der Aktualisierung „1 oben“ lautet.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Lesezeichen2 befindet sich unter diesem Feld und enthält die Fußnote Nummer 2, daher wird im Feld „2 unten“ angezeigt.
    // Das Flag \f sorgt dafür, dass die Nummer 2 im gleichen Format wie die Fußnotennummer im eigentlichen Text erscheint.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");
}

/// <summary>
/// Verwendet einen Dokument-Builder, um ein NOTEREF-Feld mit angegebenen Eigenschaften einzufügen.
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
/// Verwendet einen Dokumentersteller, um ein benanntes Lesezeichen mit einer Fußnote am Ende einzufügen.
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
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
