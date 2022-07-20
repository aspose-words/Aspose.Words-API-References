---
title: FieldToa
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das TOA-Feld.
type: docs
weight: 2370
url: /de/net/aspose.words.fields/fieldtoa/
---
## FieldToa class

Implementiert das TOA-Feld.

```csharp
public class FieldToa : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldToa](fieldtoa)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoa/bookmarkname) { get; set; } | Ruft den Namen des Lesezeichens ab oder legt ihn fest, das den Teil des Dokuments markiert, der zum Erstellen der Tabelle verwendet wurde. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [EntryCategory](../../aspose.words.fields/fieldtoa/entrycategory) { get; set; } | Holt oder setzt die integrale Kategorie für Einträge, die in der Tabelle enthalten sind. |
| [EntrySeparator](../../aspose.words.fields/fieldtoa/entryseparator) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um einen Eintrag im Rechtsgrundlagenverzeichnis von seiner Seitenzahl zu trennen. |
| [Format](../../aspose.words.fields/field/format) { get; } | erhält a[`FieldFormat`](../fieldformat) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldtoa/pagenumberlistseparator) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um zwei Seitenzahlen in einer Seitenzahlenliste zu trennen. |
| [PageRangeSeparator](../../aspose.words.fields/fieldtoa/pagerangeseparator) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um den Anfang und das Ende eines Seitenbereichs zu trennen. |
| [RemoveEntryFormatting](../../aspose.words.fields/fieldtoa/removeentryformatting) { get; set; } | Ruft ab oder legt fest, ob die Formatierung des Eintragstexts im Dokument aus dem Eintrag im Rechtsgrundlagenverzeichnis entfernt werden soll. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [SequenceName](../../aspose.words.fields/fieldtoa/sequencename) { get; set; } | Liest oder setzt den Namen einer Sequenz, deren Nummer in der Seitennummer enthalten ist. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoa/sequenceseparator) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ruft den Microsoft Word-Feldtyp ab. |
| [UseHeading](../../aspose.words.fields/fieldtoa/useheading) { get; set; } | Ruft ab oder legt fest, ob die Kategorieüberschrift für die Einträge in einem Rechtsgrundlagenverzeichnis eingeschlossen werden soll. |
| [UsePassim](../../aspose.words.fields/fieldtoa/usepassim) { get; set; } | Ruft ab oder legt fest, ob fünf oder mehr verschiedene Seitenverweise auf dieselbe Autorität durch "passim" ersetzt werden sollen, was verwendet wird, um anzuzeigen, dass ein Wort oder eine Passage häufig in der zitierten Arbeit vorkommt. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen (oder Feldende, wenn kein Trennzeichen vorhanden ist) zurück. |
| [Remove](../../aspose.words.fields/field/remove)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines Elternknotens ist, wird sein Elternabsatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben **Null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Führt das Feld Unlink aus. |
| [Update](../../aspose.words.fields/field/update)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Erstellt ein Rechtsgrundlagenverzeichnis (d. h. eine Liste der Verweise in einem Rechtsdokument, wie z. B. Verweise auf Fälle, Gesetze und Regeln, zusammen mit den Nummern der Seiten, auf denen die Verweise erscheinen) unter Verwendung der von TA angegebenen Einträge Felder.

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

* class [Field](../field)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
