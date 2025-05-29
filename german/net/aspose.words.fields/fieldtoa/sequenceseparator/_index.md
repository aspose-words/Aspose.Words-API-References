---
title: FieldToa.SequenceSeparator
linktitle: SequenceSeparator
articleTitle: SequenceSeparator
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldToa SequenceSeparator-Eigenschaft – passen Sie die Zeichenfolge zum Trennen von Sequenz- und Seitenzahlen für mehr Übersichtlichkeit einfach an.
type: docs
weight: 90
url: /de/net/aspose.words.fields/fieldtoa/sequenceseparator/
---
## FieldToa.SequenceSeparator property

Ruft die Zeichenfolge ab oder legt sie fest, die zum Trennen von Sequenznummern und Seitenzahlen verwendet wird.

```csharp
public string SequenceSeparator { get; set; }
```

## Beispiele

Zeigt, wie Sie mithilfe der Felder TOA und TA ein Rechtsgrundlagenverzeichnis erstellen und anpassen.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Fügen Sie ein TOA-Feld ein, das für jedes TA-Feld im Dokument einen Eintrag erstellt.
    // Anzeige langer Zitate und Seitenzahlen für jeden Eintrag.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Legen Sie die Eintragskategorie für unsere Tabelle fest. Diese TOA enthält jetzt nur noch TA-Felder
    // die einen übereinstimmenden Wert in ihrer EntryCategory-Eigenschaft haben.
    fieldToa.EntryCategory = "1";

    // Darüber hinaus lautet die Kategorie des Rechtsgrundlagenverzeichnisses bei Index 1 „Fälle“,
    // was als Titel unserer Tabelle angezeigt wird, wenn wir diese Variable auf „true“ setzen.
    fieldToa.UseHeading = true;

    // Wir können TA-Felder weiter filtern, indem wir ein Lesezeichen benennen, das besagt, dass sie innerhalb der TOA-Grenzen liegen müssen.
    fieldToa.BookmarkName = "MyBookmark";

    // Standardmäßig wird eine seitenbreite Registerkarte mit gepunkteter Linie zwischen den Zitaten des TA-Felds angezeigt
    // und seine Seitenzahl. Wir können es durch jeden beliebigen Text ersetzen, den wir in diese Eigenschaft einfügen.
    // Durch das Einfügen eines Tabulatorzeichens bleibt der ursprüngliche Tabulator erhalten.
    fieldToa.EntrySeparator = " \t p.";

    // Wenn wir mehrere TA-Einträge haben, die das gleiche lange Zitat teilen,
    // Alle entsprechenden Seitenzahlen werden in einer Zeile angezeigt.
    // Wir können diese Eigenschaft verwenden, um eine Zeichenfolge anzugeben, die ihre Seitenzahlen trennt.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Wir können dies auf „true“ setzen, damit in unserer Tabelle das Wort „passim“ angezeigt wird.
    // wenn sich fünf oder mehr Seitenzahlen in einer Zeile befinden.
    fieldToa.UsePassim = true;

    // Ein TA-Feld kann sich auf einen Seitenbereich beziehen.
    // Wir können hier eine Zeichenfolge angeben, die zwischen den Start- und Endseitenzahlen für solche Bereiche angezeigt wird.
    fieldToa.PageRangeSeparator = " to ";

    // Das Format aus den TA-Feldern wird in unsere Tabelle übernommen.
    // Wir können dies deaktivieren, indem wir das Flag RemoveEntryFormatting setzen.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Dieses TA-Feld erscheint nicht als Eintrag im TOA, da es außerhalb liegt
    // die Grenzen des Lesezeichens, die durch die BookmarkName-Eigenschaft des TOA angegeben werden.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Dieses TA-Feld befindet sich innerhalb des Lesezeichens,
    // aber die Eintragskategorie stimmt nicht mit der der Tabelle überein, daher wird sie nicht in das TA-Feld aufgenommen.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Dieser Eintrag wird in der Tabelle angezeigt.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // Eine TOA-Tabelle zeigt keine Kurzzitate an,
    // aber wir können sie als Abkürzung verwenden, um auf umfangreiche Quellnamen zu verweisen, auf die mehrere TA-Felder verweisen.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Wir können die Seitenzahl mit den folgenden Eigenschaften fett/kursiv formatieren.
    // Wir werden diese Effekte immer noch sehen, wenn wir unsere Tabelle so einstellen, dass die Formatierung ignoriert wird.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // Wir können TA-Felder so konfigurieren, dass ihre TOA-Einträge auf einen Seitenbereich verweisen, über den sich ein Lesezeichen erstreckt.
    // Beachten Sie, dass dieser Eintrag auf dieselbe Quelle wie der obige verweist, um eine Zeile in unserer Tabelle gemeinsam zu nutzen.
    // Diese Zeile enthält die Seitenzahl des obigen Eintrags und den Seitenbereich dieses Eintrags.
    // mit der Seitenliste der Tabelle und den Seitenzahlenbereichstrennzeichen zwischen den Seitenzahlen.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // Wenn wir die Funktion „Passim“ unserer Tabelle aktiviert haben, wird sie durch 5 oder mehr TA-Einträge mit derselben Quelle aufgerufen.
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

* class [FieldToa](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
