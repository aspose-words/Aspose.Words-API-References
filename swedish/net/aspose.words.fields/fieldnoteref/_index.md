---
title: FieldNoteRef
second_title: Aspose.Words för .NET API Referens
description: Implementerar NOTEREF-fältet.
type: docs
weight: 2050
url: /sv/net/aspose.words.fields/fieldnoteref/
---
## FieldNoteRef class

Implementerar NOTEREF-fältet.

```csharp
public class FieldNoteRef : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldNoteRef](fieldnoteref)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldnoteref/bookmarkname) { get; set; } | Hämtar eller ställer in namnet på bokmärket. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end) { get; } | Hämtar noden som representerar fältänden. |
| [Format](../../aspose.words.fields/field/format) { get; } | Får en[`FieldFormat`](../fieldformat) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [InsertHyperlink](../../aspose.words.fields/fieldnoteref/inserthyperlink) { get; set; } | Hämtar eller ställer in om en hyperlänk ska infogas till det bokmärkta stycket. |
| [InsertReferenceMark](../../aspose.words.fields/fieldnoteref/insertreferencemark) { get; set; } | Infogar referensmärket med samma teckenformatering som stilen Fotnotsreferens eller slutnotsreferens. |
| [InsertRelativePosition](../../aspose.words.fields/fieldnoteref/insertrelativeposition) { get; set; } | Hämtar eller ställer in om en relativ position för det bokmärkta stycket ska infogas. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [Start](../../aspose.words.fields/field/start) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Infogar märket för fotnoten eller slutnoten som markeras med det angivna bokmärket.

### Exempel

Visar för att infoga NOTEREF-fält och ändra deras utseende.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Skapa ett bokmärke med en fotnot som NOTEREF-fältet refererar till.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // Detta NOTEREF-fält visar numret på fotnoten inuti det refererade bokmärket.
    // Genom att ställa in egenskapen InsertHyperlink kan vi hoppa till bokmärket genom att Ctrl + klicka på fältet i Microsoft Word.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // När du använder flaggan \p, efter fotnotsnumret, visar fältet även bokmärkets position i förhållande till fältet.
    // Bokmärke1 är ovanför detta fält och innehåller fotnot nummer 1, så resultatet blir "1 ovan" vid uppdatering.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bokmärke2 är under detta fält och innehåller fotnot nummer 2, så fältet kommer att visa "2 nedan".
    // Flaggan \f gör att siffran 2 visas i samma format som fotnotsnummeretiketten i själva texten.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");

/// <summary>
/// Använder en dokumentbyggare för att infoga ett NOTEREF-fält med specificerade egenskaper.
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

* class [Field](../field)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
