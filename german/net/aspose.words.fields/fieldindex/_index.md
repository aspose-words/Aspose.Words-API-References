---
title: FieldIndex Class
linktitle: FieldIndex
articleTitle: FieldIndex
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldIndex, um mühelos INDEX-Felder in Ihre Dokumente zu implementieren. Verbessern Sie noch heute Ihr Dokumentenmanagement!
type: docs
weight: 2470
url: /de/net/aspose.words.fields/fieldindex/
---
## FieldIndex class

Implementiert das INDEX-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldIndex : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldIndex](fieldindex/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldindex/bookmarkname/) { get; set; } | Ruft den Namen des Lesezeichens ab oder legt ihn fest, das den Teil des Dokuments markiert, der zum Erstellen des Index verwendet wird. |
| [CrossReferenceSeparator](../../aspose.words.fields/fieldindex/crossreferenceseparator/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die zum Trennen von Querverweisen und anderen Einträgen verwendet wird. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [EntryType](../../aspose.words.fields/fieldindex/entrytype/) { get; set; } | Ruft einen Indexeintragstyp ab oder legt ihn fest, der zum Erstellen des Index verwendet wird. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [HasPageNumberSeparator](../../aspose.words.fields/fieldindex/haspagenumberseparator/) { get; } | Ruft einen Wert ab, der angibt, ob ein Seitenzahlentrennzeichen durch den Code des Felds überschrieben wird. |
| [HasSequenceName](../../aspose.words.fields/fieldindex/hassequencename/) { get; } | Ruft einen Wert ab, der angibt, ob beim Erstellen des Feldergebnisses eine Sequenz verwendet werden soll. |
| [Heading](../../aspose.words.fields/fieldindex/heading/) { get; set; } | Ruft eine Überschrift ab oder legt sie fest, die am Anfang jedes Eintragssatzes für einen beliebigen Buchstaben angezeigt wird. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LanguageId](../../aspose.words.fields/fieldindex/languageid/) { get; set; } | Ruft die zum Generieren des Index verwendete Sprach-ID ab oder legt sie fest. |
| [LetterRange](../../aspose.words.fields/fieldindex/letterrange/) { get; set; } | Ruft einen Buchstabenbereich ab oder legt ihn fest, auf den der Index beschränkt wird. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [NumberOfColumns](../../aspose.words.fields/fieldindex/numberofcolumns/) { get; set; } | Ruft die Anzahl der Spalten pro Seite ab, die beim Erstellen des Index verwendet werden, oder legt diese fest. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldindex/pagenumberlistseparator/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die zum Trennen zweier Seitenzahlen in einer Seitenzahlenliste verwendet wird. |
| [PageNumberSeparator](../../aspose.words.fields/fieldindex/pagenumberseparator/) { get; set; } | Ruft die Zeichenfolge ab, die zum Trennen eines Indexeintrags und seiner Seitenzahl verwendet wird, oder legt diese fest. |
| [PageRangeSeparator](../../aspose.words.fields/fieldindex/pagerangeseparator/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um Anfang und Ende eines Seitenbereichs zu trennen. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [RunSubentriesOnSameLine](../../aspose.words.fields/fieldindex/runsubentriesonsameline/) { get; set; } | Ruft ab oder legt fest, ob Untereinträge in derselben Zeile wie der Haupteintrag ausgeführt werden. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [SequenceName](../../aspose.words.fields/fieldindex/sequencename/) { get; set; } | Ruft den Namen einer Sequenz ab oder legt ihn fest, deren Nummer in der Seitenzahl enthalten ist. |
| [SequenceSeparator](../../aspose.words.fields/fieldindex/sequenceseparator/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die zum Trennen von Sequenznummern und Seitenzahlen verwendet wird. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |
| [UseYomi](../../aspose.words.fields/fieldindex/useyomi/) { get; set; } | Ruft ab oder legt fest, ob die Verwendung von Yomi-Text für Indexeinträge aktiviert werden soll. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern werden einbezogen. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt die Feldverknüpfung aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Erstellt einen Index unter Verwendung der durch die XE-Felder angegebenen Indexeinträge und fügt diesen Index an dieser Stelle im Dokument ein.

## Beispiele

Zeigt, wie Sie ein INDEX-Feld erstellen und es dann mithilfe von XE-Feldern mit Einträgen füllen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt den Text-Eigenschaftswert des XE-Felds auf der linken Seite an
// und die Seite mit dem XE-Feld auf der rechten Seite.
// Wenn die XE-Felder den gleichen Wert in ihrer Eigenschaft "Text" haben,
// Das INDEX-Feld gruppiert sie in einem Eintrag.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Konfigurieren Sie das INDEX-Feld nur so, dass XE-Felder angezeigt werden, die innerhalb der Grenzen liegen
// eines Lesezeichens mit dem Namen „MainBookmark“, dessen „EntryType“-Eigenschaften den Wert „A“ haben.
// Sowohl für INDEX- als auch für XE-Felder verwendet die Eigenschaft „EntryType“ nur das erste Zeichen ihres Zeichenfolgenwerts.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// Beginnen Sie das Lesezeichen auf einer neuen Seite mit einem Namen, der dem Wert entspricht
// der Eigenschaft „BookmarkName“ des INDEX-Felds.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// Das INDEX-Feld wird diesen Eintrag aufnehmen, da er sich innerhalb des Lesezeichens befindet.
// und sein Eintragstyp entspricht auch dem Eintragstyp des INDEX-Felds.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Fügen Sie ein XE-Feld ein, das nicht im INDEX angezeigt wird, da die Eintragstypen nicht übereinstimmen.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Beenden Sie das Lesezeichen und fügen Sie anschließend ein XE-Feld ein.
// Es ist vom gleichen Typ wie das INDEX-Feld, wird aber nicht angezeigt
// da es außerhalb der Grenzen des Lesezeichens liegt.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Zeigt, wie Sie ein INDEX-Feld mithilfe von XE-Feldern mit Einträgen füllen und auch sein Erscheinungsbild ändern.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt auf der linken Seite den Text-Eigenschaftswert des XE-Felds an,
// und die Nummer der Seite, die rechts das XE-Feld enthält.
// Wenn die XE-Felder den gleichen Wert in ihrer Eigenschaft "Text" haben,
// Das INDEX-Feld gruppiert sie in einem Eintrag.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Wenn Sie den Wert dieser Eigenschaft auf „A“ setzen, werden alle Einträge nach ihrem Anfangsbuchstaben gruppiert.
// und platzieren Sie diesen Buchstaben als Großbuchstaben über jeder Gruppe.
index.Heading = "A";

// Legen Sie fest, dass die durch das INDEX-Feld erstellte Tabelle sich über zwei Spalten erstreckt.
index.NumberOfColumns = "2";

// Legen Sie fest, dass alle Einträge mit Anfangsbuchstaben außerhalb des Zeichenbereichs „ac“ weggelassen werden.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Die nächsten beiden XE-Felder werden unter der Überschrift „A“ angezeigt.
// mit den jeweiligen Textformatierungen, die auch auf die Seitenzahlen angewendet werden.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// Die nächsten beiden XE-Felder stehen im Inhaltsverzeichnis der INDEX-Felder unter der Überschrift „B“ und „C“.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// INDEX-Felder sortieren alle Einträge alphabetisch, sodass dieser Eintrag mit den anderen beiden unter „A“ angezeigt wird.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Dieser Eintrag wird nicht angezeigt, da er mit dem Buchstaben "D" beginnt,
// der außerhalb des „ac“-Zeichenbereichs liegt, der durch die LetterRange-Eigenschaft des INDEX-Felds definiert wird.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
