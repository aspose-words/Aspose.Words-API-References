---
title: FieldPageRef.InsertHyperlink
second_title: Aspose.Words för .NET API Referens
description: FieldPageRef fast egendom. Hämtar eller ställer in om en hyperlänk ska infogas till det bokmärkta stycket.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldpageref/inserthyperlink/
---
## FieldPageRef.InsertHyperlink property

Hämtar eller ställer in om en hyperlänk ska infogas till det bokmärkta stycket.

```csharp
public bool InsertHyperlink { get; set; }
```

### Exempel

Visar för att infoga PAGEREF-fält för att visa den relativa platsen för bokmärken.

```csharp
public void FieldPageRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    InsertAndNameBookmark(builder, "MyBookmark1");

    // Infoga ett PAGEREF-fält som visar vilken sida ett bokmärke finns på.
    // Ställ in flaggan InsertHyperlink för att få fältet att även fungera som en klickbar länk till bokmärket.
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h", 
        InsertFieldPageRef(builder, "MyBookmark3", true, false, "Hyperlink to Bookmark3, on page: ").GetFieldCode());

    // Vi kan använda flaggan \p för att få PAGEREF-fältet att visas
    // bokmärkets position i förhållande till fältets position.
    // Bokmärke1 är på samma sida och ovanför detta fält, så det här fältets visade resultat kommer att vara "ovanför".
    Assert.AreEqual(" PAGEREF  MyBookmark1 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark1", true, true, "Bookmark1 is ").GetFieldCode());

    // Bokmärke2 kommer att finnas på samma sida och under det här fältet, så det här fältets visade resultat kommer att vara "nedan".
    Assert.AreEqual(" PAGEREF  MyBookmark2 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark2", true, true, "Bookmark2 is ").GetFieldCode());

    // Bokmärke3 kommer att finnas på en annan sida, så fältet kommer att visa "på sida 2".
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark3", true, true, "Bookmark3 is ").GetFieldCode());

    InsertAndNameBookmark(builder, "MyBookmark2");
    builder.InsertBreak(BreakType.PageBreak);
    InsertAndNameBookmark(builder, "MyBookmark3");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.PAGEREF.docx");

/// <summary>
/// Använder en dokumentbyggare för att infoga ett PAGEREF-fält och ställer in dess egenskaper.
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
/// Använder en dokumentbyggare för att infoga ett namngivet bokmärke.
/// </summary>
private static void InsertAndNameBookmark(DocumentBuilder builder, string bookmarkName)
{
    builder.StartBookmark(bookmarkName);
    builder.Writeln($"Contents of bookmark \"{bookmarkName}\".");
    builder.EndBookmark(bookmarkName);
}
```

### Se även

* class [FieldPageRef](../)
* namnutrymme [Aspose.Words.Fields](../../fieldpageref/)
* hopsättning [Aspose.Words](../../../)


