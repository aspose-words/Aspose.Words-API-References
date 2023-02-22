---
title: FieldPageRef.InsertHyperlink
second_title: Aspose.Words für .NET-API-Referenz
description: FieldPageRef eigendom. Ruft ab oder legt fest ob ein Hyperlink zum mit Lesezeichen versehenen Absatz eingefügt werden soll.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldpageref/inserthyperlink/
---
## FieldPageRef.InsertHyperlink property

Ruft ab oder legt fest, ob ein Hyperlink zum mit Lesezeichen versehenen Absatz eingefügt werden soll.

```csharp
public bool InsertHyperlink { get; set; }
```

### Beispiele

Zeigt das Einfügen von PAGEREF-Feldern an, um die relative Position von Lesezeichen anzuzeigen.

```csharp
public void FieldPageRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    InsertAndNameBookmark(builder, "MyBookmark1");

    // Fügt ein PAGEREF-Feld ein, das anzeigt, auf welcher Seite sich ein Lesezeichen befindet.
    // Setzen Sie das InsertHyperlink-Flag, damit das Feld auch als anklickbarer Link zum Lesezeichen fungiert.
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h", 
        InsertFieldPageRef(builder, "MyBookmark3", true, false, "Hyperlink to Bookmark3, on page: ").GetFieldCode());

    // Wir können das Flag \p verwenden, um das Feld PAGEREF anzuzeigen
    // die Position des Lesezeichens relativ zur Position des Felds.
    // Lesezeichen1 befindet sich auf derselben Seite und über diesem Feld, daher wird das angezeigte Ergebnis dieses Felds "oben" sein.
    Assert.AreEqual(" PAGEREF  MyBookmark1 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark1", true, true, "Bookmark1 is ").GetFieldCode());

    // Lesezeichen2 befindet sich auf derselben Seite und unter diesem Feld, daher wird das angezeigte Ergebnis dieses Felds "unterhalb" sein.
    Assert.AreEqual(" PAGEREF  MyBookmark2 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark2", true, true, "Bookmark2 is ").GetFieldCode());

    // Lesezeichen3 befindet sich auf einer anderen Seite, daher wird im Feld "auf Seite 2" angezeigt.
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark3", true, true, "Bookmark3 is ").GetFieldCode());

    InsertAndNameBookmark(builder, "MyBookmark2");
    builder.InsertBreak(BreakType.PageBreak);
    InsertAndNameBookmark(builder, "MyBookmark3");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.PAGEREF.docx");

/// <summary>
/// Verwendet einen Document Builder, um ein PAGEREF-Feld einzufügen und seine Eigenschaften festzulegen.
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
/// Verwendet einen Document Builder, um ein benanntes Lesezeichen einzufügen.
/// </summary>
private static void InsertAndNameBookmark(DocumentBuilder builder, string bookmarkName)
{
    builder.StartBookmark(bookmarkName);
    builder.Writeln($"Contents of bookmark \"{bookmarkName}\".");
    builder.EndBookmark(bookmarkName);
}
```

### Siehe auch

* class [FieldPageRef](../)
* namensraum [Aspose.Words.Fields](../../fieldpageref/)
* Montage [Aspose.Words](../../../)


