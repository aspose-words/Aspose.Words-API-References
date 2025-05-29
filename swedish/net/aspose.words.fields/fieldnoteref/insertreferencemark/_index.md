---
title: FieldNoteRef.InsertReferenceMark
linktitle: InsertReferenceMark
articleTitle: InsertReferenceMark
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldNoteRef InsertReferenceMark för att smidigt infoga formaterade referensmarkeringar, vilket förbättrar dokumentets tydlighet och professionalism.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldnoteref/insertreferencemark/
---
## FieldNoteRef.InsertReferenceMark property

Infogar referenstecknet med samma teckenformatering som fotnotsreferens eller slutnotsreferensformatet.

```csharp
public bool InsertReferenceMark { get; set; }
```

## Exempel

Visar hur man infogar NOTEREF-fält och ändrar deras utseende.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Skapa ett bokmärke med en fotnot som NOTEREF-fältet ska referera till.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // Detta NOTEREF-fält visar numret på fotnoten inuti det refererade bokmärket.
    // Genom att ställa in egenskapen InsertHyperlink kan vi hoppa till bokmärket genom att Ctrl + klicka på fältet i Microsoft Word.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // När man använder \p-flaggan, efter fotnotsnumret, visar fältet även bokmärkets position i förhållande till fältet.
    // Bokmärke1 finns ovanför detta fält och innehåller fotnot nummer 1, så resultatet blir "1 ovanför" vid uppdatering.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bokmärke2 finns under detta fält och innehåller fotnot nummer 2, så fältet kommer att visa "2 nedan".
    // Flaggan \f gör att siffran 2 visas i samma format som fotnotens numreringsetikett i den faktiska texten.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");
}

/// <summary>
/// Använder en dokumentbyggare för att infoga ett NOTEREF-fält med angivna egenskaper.
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
/// Använder en dokumentbyggare för att infoga ett namngivet bokmärke med en fotnot i slutet.
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

### Se även

* class [FieldNoteRef](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
