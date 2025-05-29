---
title: FieldPageRef.InsertRelativePosition
linktitle: InsertRelativePosition
articleTitle: InsertRelativePosition
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen InsertRelativePosition i FieldPageRef förbättrar dokumentnavigering genom att hantera bokmärkta styckepositioner effektivt.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldpageref/insertrelativeposition/
---
## FieldPageRef.InsertRelativePosition property

Hämtar eller anger om en relativ position för det bokmärkta stycket ska infogas.

```csharp
public bool InsertRelativePosition { get; set; }
```

## Exempel

Visar hur man infogar SIDREF-fält för att visa bokmärkenas relativa placering.

```csharp
public void FieldPageRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    InsertAndNameBookmark(builder, "MyBookmark1");

    // Infoga ett PAGEREF-fält som visar vilken sida ett bokmärke finns på.
    // Ställ in flaggan InsertHyperlink för att göra så att fältet även fungerar som en klickbar länk till bokmärket.
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h", 
        InsertFieldPageRef(builder, "MyBookmark3", true, false, "Hyperlink to Bookmark3, on page: ").GetFieldCode());

    // Vi kan använda \p-flaggan för att få PAGEREF-fältet att visas
    // bokmärkets position i förhållande till fältets position.
    // Bokmärke1 finns på samma sida och ovanför detta fält, så det visade resultatet i detta fält kommer att vara "ovanför".
    Assert.AreEqual(" PAGEREF  MyBookmark1 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark1", true, true, "Bookmark1 is ").GetFieldCode());

    // Bokmärke2 kommer att finnas på samma sida och under detta fält, så det visade resultatet i detta fält kommer att vara "nedanför".
    Assert.AreEqual(" PAGEREF  MyBookmark2 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark2", true, true, "Bookmark2 is ").GetFieldCode());

    // Bokmärke3 kommer att finnas på en annan sida, så fältet kommer att visa "på sida 2".
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
/// Använder en dokumentbyggare för att infoga ett PAGEREF-fält och anger dess egenskaper.
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
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
