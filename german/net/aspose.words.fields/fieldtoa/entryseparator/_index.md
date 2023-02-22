---
title: FieldToa.EntrySeparator
second_title: Aspose.Words für .NET-API-Referenz
description: FieldToa eigendom. Ruft die Zeichenfolge ab oder legt sie fest die verwendet wird um einen Eintrag im Rechtsgrundlagenverzeichnis von seiner Seitenzahl zu trennen.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldtoa/entryseparator/
---
## FieldToa.EntrySeparator property

Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um einen Eintrag im Rechtsgrundlagenverzeichnis von seiner Seitenzahl zu trennen.

```csharp
public string EntrySeparator { get; set; }
```

### Beispiele

Zeigt, wie ein Rechtsgrundlagenverzeichnis mithilfe von TOA- und TA-Feldern erstellt und angepasst wird.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Fügen Sie ein TOA-Feld ein, das einen Eintrag für jedes TA-Feld im Dokument erstellt,
    // Anzeigen von langen Zitaten und Seitenzahlen für jeden Eintrag.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Legen Sie die Eintragskategorie für unsere Tabelle fest. Diese TOA enthält jetzt nur noch TA-Felder
    // die einen übereinstimmenden Wert in ihrer EntryCategory-Eigenschaft haben.
    fieldToa.EntryCategory = "1";

    // Darüber hinaus ist die Kategorie des Rechtsträgerverzeichnisses bei Index 1 "Fälle",
    // was als Titel unserer Tabelle erscheint, wenn wir diese Variable auf true setzen.
    fieldToa.UseHeading = true;

    // Wir können TA-Felder weiter filtern, indem wir ein Lesezeichen benennen, das sie innerhalb der TOA-Grenzen haben müssen.
    fieldToa.BookmarkName = "MyBookmark";

    // Standardmäßig erscheint ein seitenweiter Tabulator mit gepunkteter Linie zwischen dem Zitat des TA-Felds
    // und seine Seitenzahl. Wir können es durch jeden Text ersetzen, den wir dieser Eigenschaft hinzufügen.
    // Durch das Einfügen eines Tabulatorzeichens wird der ursprüngliche Tabulator beibehalten.
    fieldToa.EntrySeparator = " \t p.";

    // Wenn wir mehrere TA-Einträge haben, die dasselbe lange Zitat teilen,
    // Alle ihre jeweiligen Seitenzahlen werden in einer Zeile angezeigt.
    // Wir können diese Eigenschaft verwenden, um eine Zeichenfolge anzugeben, die ihre Seitenzahlen trennt.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Wir können dies auf true setzen, damit unsere Tabelle das Wort "passim" anzeigt
    // wenn es fünf oder mehr Seitenzahlen in einer Zeile gibt.
    fieldToa.UsePassim = true;

    // Ein TA-Feld kann auf eine Reihe von Seiten verweisen.
    // Wir können hier einen String angeben, der zwischen der Start- und Endseitenzahl für solche Bereiche erscheint.
    fieldToa.PageRangeSeparator = " to ";

    // Das Format aus den TA-Feldern wird in unsere Tabelle übernommen.
    // Wir können dies deaktivieren, indem wir das RemoveEntryFormatting-Flag setzen.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Dieses TA-Feld erscheint nicht als Eintrag in der TOA, da es außerhalb liegt
    // die Grenzen des Lesezeichens, die die Eigenschaft BookmarkName des TOA angibt.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Dieses TA-Feld befindet sich innerhalb des Lesezeichens,
    // aber die Eintragskategorie stimmt nicht mit der der Tabelle überein, also wird sie nicht im TA-Feld enthalten sein.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Dieser Eintrag erscheint in der Tabelle.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // Eine TOA-Tabelle zeigt keine Kurzzitate an,
    // aber wir können sie als Abkürzung verwenden, um auf umfangreiche Quellnamen zu verweisen, auf die mehrere TA-Felder verweisen.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Wir können die Seitenzahl formatieren, um sie fett/kursiv zu machen, indem wir die folgenden Eigenschaften verwenden.
    // Wir werden diese Effekte immer noch sehen, wenn wir unsere Tabelle so einstellen, dass sie die Formatierung ignoriert.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // Wir können TA-Felder so konfigurieren, dass ihre TOA-Einträge auf eine Reihe von Seiten verweisen, über die sich ein Lesezeichen erstreckt.
    // Beachten Sie, dass sich dieser Eintrag auf dieselbe Quelle wie der obige bezieht, um eine Zeile in unserer Tabelle gemeinsam zu nutzen.
    // Diese Zeile enthält die Seitennummer des obigen Eintrags und den Seitenbereich dieses Eintrags,
    // mit der Seitenliste der Tabelle und Trennzeichen für den Seitennummernbereich zwischen den Seitennummern.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // Wenn wir die "Passim"-Funktion unserer Tabelle aktiviert haben, wird sie bei 5 oder mehr TA-Einträgen mit derselben Quelle aufgerufen.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");

private static FieldTA InsertToaEntry(DocumentBuilder builder, string entryCategory, string longCitation)
{
    FieldTA field = (FieldTA)builder.InsertField(FieldType.FieldTOAEntry, false);
    field.EntryCategory = entryCategory;
    field.LongCitation = longCitation;

    builder.InsertBreak(BreakType.PageBreak);

    return field;
}
```

### Siehe auch

* class [FieldToa](../)
* namensraum [Aspose.Words.Fields](../../fieldtoa/)
* Montage [Aspose.Words](../../../)


