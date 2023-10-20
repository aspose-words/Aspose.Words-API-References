---
title: FieldToa Class
linktitle: FieldToa
articleTitle: FieldToa
second_title: Aspose.Words für .NET
description: Aspose.Words.Fields.FieldToa klas. Implementiert das TOAFeld in C#.
type: docs
weight: 2520
url: /de/net/aspose.words.fields/fieldtoa/
---
## FieldToa class

Implementiert das TOA-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldToa : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldToa](fieldtoa/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoa/bookmarkname/) { get; set; } | Ruft den Namen des Lesezeichens ab, das den Teil des Dokuments markiert, der zum Erstellen der Tabelle verwendet wird, oder legt diesen fest. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [EntryCategory](../../aspose.words.fields/fieldtoa/entrycategory/) { get; set; } | Ruft die Integralkategorie für in der Tabelle enthaltene Einträge ab oder legt diese fest. |
| [EntrySeparator](../../aspose.words.fields/fieldtoa/entryseparator/) { get; set; } | Ruft die Zeichenfolge ab, die zum Trennen eines Normverzeichniseintrags und seiner Seitenzahl verwendet wird, oder legt diese fest. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ruft a ab[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldtoa/pagenumberlistseparator/) { get; set; } | Ruft die Zeichenfolge ab, die zum Trennen zweier Seitenzahlen in einer Seitenzahlenliste verwendet wird, oder legt diese fest. |
| [PageRangeSeparator](../../aspose.words.fields/fieldtoa/pagerangeseparator/) { get; set; } | Ruft die Zeichenfolge ab, die zum Trennen des Anfangs und Endes eines Seitenbereichs verwendet wird, oder legt diese fest. |
| [RemoveEntryFormatting](../../aspose.words.fields/fieldtoa/removeentryformatting/) { get; set; } | Ruft ab oder legt fest, ob die Formatierung des Eintragstexts im Dokument aus dem Eintrag im Rechtsgrundlagenverzeichnis entfernt werden soll. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab, der zwischen dem Feldtrennzeichen und dem Feldende liegt, oder legt diesen fest. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`Null` . |
| [SequenceName](../../aspose.words.fields/fieldtoa/sequencename/) { get; set; } | Ruft den Namen einer Sequenz ab oder legt diesen fest, deren Nummer in der Seitenzahl enthalten ist. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoa/sequenceseparator/) { get; set; } | Ruft die Zeichenfolge ab, die zum Trennen von Sequenznummern und Seitenzahlen verwendet wird, oder legt diese fest. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |
| [UseHeading](../../aspose.words.fields/fieldtoa/useheading/) { get; set; } | Ruft ab oder legt fest, ob die Kategorieüberschrift für die Einträge in einem Rechtsgrundlagenverzeichnis enthalten sein soll. |
| [UsePassim](../../aspose.words.fields/fieldtoa/usepassim/) { get; set; } | Ruft ab oder legt fest, ob fünf oder mehr verschiedene Seitenverweise auf dieselbe Autorität durch „passim“ ersetzt werden sollen, was verwendet wird, um anzugeben, dass ein Wort oder eine Passage häufig im zitierten Werk vorkommt. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl der Feldcode als auch das Feldergebnis der untergeordneten Felder sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte child seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`Null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld unlink aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Erstellt unter Verwendung der von TA angegebenen -Einträge ein Autoritätsverzeichnis (d. h. eine Liste der Verweise in einem Rechtsdokument, z. B. Verweise auf Fälle, Gesetze und Regeln, zusammen mit den Nummern der Seiten, auf denen die Verweise erscheinen). Felder.

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

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
