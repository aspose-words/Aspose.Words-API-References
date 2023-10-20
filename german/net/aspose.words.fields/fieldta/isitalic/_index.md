---
title: FieldTA.IsItalic
linktitle: IsItalic
articleTitle: IsItalic
second_title: Aspose.Words für .NET
description: FieldTA IsItalic eigendom. Ruft ab oder legt fest ob eine kursive Formatierung auf die Seitenzahl für den Eintrag angewendet werden soll in C#.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldta/isitalic/
---
## FieldTA.IsItalic property

Ruft ab oder legt fest, ob eine kursive Formatierung auf die Seitenzahl für den Eintrag angewendet werden soll.

```csharp
public bool IsItalic { get; set; }
```

## Beispiele

Zeigt, wie man mithilfe von TOA- und TA-Feldern ein Autoritätsverzeichnis erstellt und anpasst.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Ein TOA-Feld einfügen, das einen Eintrag für jedes TA-Feld im Dokument erstellt,
    // Anzeige langer Zitate und Seitenzahlen für jeden Eintrag.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Legen Sie die Eintragskategorie für unsere Tabelle fest. Diese TOA umfasst jetzt nur noch TA-Felder
    // die einen passenden Wert in ihrer EntryCategory-Eigenschaft haben.
    fieldToa.EntryCategory = "1";

    // Darüber hinaus lautet die Kategorie „Tabelle der Behörden“ auf Index 1 „Fälle“.
    // was als Titel unserer Tabelle angezeigt wird, wenn wir diese Variable auf true setzen.
    fieldToa.UseHeading = true;

    // Wir können TA-Felder weiter filtern, indem wir ein Lesezeichen benennen, das besagt, dass sie innerhalb der TOA-Grenzen liegen müssen.
    fieldToa.BookmarkName = "MyBookmark";

    // Standardmäßig wird zwischen dem Zitat des TA-Felds eine seitenweite Registerkarte mit gepunkteter Linie angezeigt
    // und seine Seitenzahl. Wir können es durch jeden Text ersetzen, den wir auf dieser Eigenschaft platzieren.
    // Durch das Einfügen eines Tabulatorzeichens bleibt der ursprüngliche Tabulator erhalten.
    fieldToa.EntrySeparator = " \t p.";

    // Wenn wir mehrere TA-Einträge haben, die dasselbe lange Zitat haben,
    // alle zugehörigen Seitenzahlen werden in einer Zeile angezeigt.
    // Wir können diese Eigenschaft verwenden, um eine Zeichenfolge anzugeben, die ihre Seitenzahlen trennt.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Wir können dies auf „true“ setzen, damit unsere Tabelle das Wort „passim“ anzeigt.
    // wenn in einer Zeile fünf oder mehr Seitenzahlen stehen.
    fieldToa.UsePassim = true;

    // Ein TA-Feld kann sich auf einen Bereich von Seiten beziehen.
    // Wir können hier eine Zeichenfolge angeben, die zwischen der Start- und Endseitennummer für solche Bereiche angezeigt wird.
    fieldToa.PageRangeSeparator = " to ";

    // Das Format aus den TA-Feldern wird in unsere Tabelle übernommen.
    // Wir können dies deaktivieren, indem wir das RemoveEntryFormatting-Flag setzen.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Dieses TA-Feld erscheint nicht als Eintrag im TOA, da es außerhalb liegt
    // die Grenzen des Lesezeichens, die die BookmarkName-Eigenschaft des TOA angibt.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Dieses TA-Feld befindet sich im Lesezeichen,
    // aber die Eintragskategorie stimmt nicht mit der der Tabelle überein, sodass das TA-Feld sie nicht enthält.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Dieser Eintrag erscheint in der Tabelle.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // Eine TOA-Tabelle zeigt keine Kurzzitate an,
    // aber wir können sie als Abkürzung verwenden, um auf umfangreiche Quellnamen zu verweisen, auf die mehrere TA-Felder verweisen.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Mit den folgenden Eigenschaften können wir die Seitenzahl so formatieren, dass sie fett/kursiv erscheint.
    // Wir werden diese Effekte immer noch sehen, wenn wir unsere Tabelle so einstellen, dass sie die Formatierung ignoriert.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // Wir können TA-Felder so konfigurieren, dass ihre TOA-Einträge auf einen Bereich von Seiten verweisen, über die sich ein Lesezeichen erstreckt.
    // Beachten Sie, dass sich dieser Eintrag auf dieselbe Quelle wie der obige bezieht, um eine Zeile in unserer Tabelle gemeinsam zu nutzen.
    // Diese Zeile enthält die Seitenzahl des obigen Eintrags und den Seitenbereich dieses Eintrags.
    // mit der Seitenliste der Tabelle und den Seitenzahlbereichstrennzeichen zwischen den Seitenzahlen.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // Wenn wir die „Passim“-Funktion unserer Tabelle aktiviert haben, wird sie bei 5 oder mehr TA-Einträgen mit derselben Quelle aufgerufen.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");
}

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

* class [FieldTA](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
