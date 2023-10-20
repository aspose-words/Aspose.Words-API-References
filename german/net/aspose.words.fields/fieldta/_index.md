---
title: FieldTA Class
linktitle: FieldTA
articleTitle: FieldTA
second_title: Aspose.Words für .NET
description: Aspose.Words.Fields.FieldTA klas. Implementiert das TAFeld in C#.
type: docs
weight: 2470
url: /de/net/aspose.words.fields/fieldta/
---
## FieldTA class

Implementiert das TA-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldTA : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldTA](fieldta/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [EntryCategory](../../aspose.words.fields/fieldta/entrycategory/) { get; set; } | Ruft die ganzzahlige Eintragskategorie ab oder legt diese fest. Dabei handelt es sich um eine Zahl, die der Reihenfolge der Kategorien entspricht. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ruft a ab[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsBold](../../aspose.words.fields/fieldta/isbold/) { get; set; } | Ruft ab oder legt fest, ob Fettformatierung auf die Seitenzahl für den Eintrag angewendet werden soll. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsItalic](../../aspose.words.fields/fieldta/isitalic/) { get; set; } | Ruft ab oder legt fest, ob eine kursive Formatierung auf die Seitenzahl für den Eintrag angewendet werden soll. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [LongCitation](../../aspose.words.fields/fieldta/longcitation/) { get; set; } | Ruft das lange Zitat für den Eintrag ab oder legt es fest. |
| [PageRangeBookmarkName](../../aspose.words.fields/fieldta/pagerangebookmarkname/) { get; set; } | Ruft den Namen des Lesezeichens ab, das einen Seitenbereich markiert, der als Seitenzahl des Eintrags eingefügt wird, oder legt diesen fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab, der zwischen dem Feldtrennzeichen und dem Feldende liegt, oder legt diesen fest. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`Null` . |
| [ShortCitation](../../aspose.words.fields/fieldta/shortcitation/) { get; set; } | Ruft das Kurzzitat für den Eintrag ab oder legt es fest. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

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

Definiert den Text und die Seitenzahl für einen Eintrag im Rechtsgrundlagenverzeichnis, der von einem TOA-Feld verwendet wird.

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
