---
title: Class FieldIndex
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.FieldIndex klas. Implementiert das INDEXFeld.
type: docs
weight: 1910
url: /de/net/aspose.words.fields/fieldindex/
---
## FieldIndex class

Implementiert das INDEX-Feld.

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
| [BookmarkName](../../aspose.words.fields/fieldindex/bookmarkname/) { get; set; } | Ruft den Namen des Lesezeichens ab oder legt ihn fest, das den Teil des Dokuments markiert, der zum Erstellen des Index verwendet wurde. |
| [CrossReferenceSeparator](../../aspose.words.fields/fieldindex/crossreferenceseparator/) { get; set; } | Ermittelt oder setzt die Zeichenfolge, die verwendet wird, um Querverweise und andere Einträge zu trennen. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [EntryType](../../aspose.words.fields/fieldindex/entrytype/) { get; set; } | Ruft einen Indexeintragstyp ab oder legt ihn fest, der zum Erstellen des Index verwendet wird. |
| [Format](../../aspose.words.fields/field/format/) { get; } | erhält a[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [HasPageNumberSeparator](../../aspose.words.fields/fieldindex/haspagenumberseparator/) { get; } | Ruft einen Wert ab, der angibt, ob ein Seitenzahlentrennzeichen durch den Feldcode überschrieben wird. |
| [HasSequenceName](../../aspose.words.fields/fieldindex/hassequencename/) { get; } | Ruft einen Wert ab, der angibt, ob bei der Ergebnisbildung des Felds eine Sequenz verwendet werden soll. |
| [Heading](../../aspose.words.fields/fieldindex/heading/) { get; set; } | Ruft eine Überschrift ab oder legt sie fest, die am Anfang jeder Gruppe von Einträgen für einen bestimmten Buchstaben erscheint. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LanguageId](../../aspose.words.fields/fieldindex/languageid/) { get; set; } | Ruft die Sprach-ID ab oder legt sie fest, die zum Generieren des Index verwendet wird. |
| [LetterRange](../../aspose.words.fields/fieldindex/letterrange/) { get; set; } | Erhält oder setzt einen Bereich von Buchstaben, auf den der Index begrenzt wird. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [NumberOfColumns](../../aspose.words.fields/fieldindex/numberofcolumns/) { get; set; } | Ruft die Anzahl der Spalten pro Seite ab oder legt sie fest, die beim Erstellen des Index verwendet werden. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldindex/pagenumberlistseparator/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um zwei Seitenzahlen in einer Seitenzahlenliste zu trennen. |
| [PageNumberSeparator](../../aspose.words.fields/fieldindex/pagenumberseparator/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um einen Indexeintrag und seine Seitennummer zu trennen. |
| [PageRangeSeparator](../../aspose.words.fields/fieldindex/pagerangeseparator/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um den Anfang und das Ende eines Seitenbereichs zu trennen. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [RunSubentriesOnSameLine](../../aspose.words.fields/fieldindex/runsubentriesonsameline/) { get; set; } | Ruft ab oder legt fest, ob Untereinträge in derselben Zeile wie der Haupteintrag ausgeführt werden. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [SequenceName](../../aspose.words.fields/fieldindex/sequencename/) { get; set; } | Liest oder setzt den Namen einer Sequenz, deren Nummer in der Seitennummer enthalten ist. |
| [SequenceSeparator](../../aspose.words.fields/fieldindex/sequenceseparator/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |
| [UseYomi](../../aspose.words.fields/fieldindex/useyomi/) { get; set; } | Ruft ab oder legt fest, ob die Verwendung von Yomi-Text für Indexeinträge aktiviert werden soll. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen (oder Feldende, wenn kein Trennzeichen vorhanden ist) zurück. |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines Elternknotens ist, wird sein Elternabsatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben **Null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld Unlink aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Erstellt einen Index unter Verwendung der durch XE-Felder angegebenen Indexeinträge und fügt diesen Index an dieser Stelle in das Dokument ein.

### Beispiele

Zeigt, wie Sie ein INDEX-Feld erstellen und es dann mithilfe von XE-Feldern mit Einträgen füllen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das einen Eintrag für jedes im Dokument gefundene XE-Feld anzeigt.
// Jeder Eintrag zeigt den Text-Eigenschaftswert des XE-Felds auf der linken Seite an
// und rechts die Seite mit dem XE-Feld.
// Wenn die XE-Felder den gleichen Wert in ihrer "Text"-Eigenschaft haben,
// das Feld INDEX gruppiert sie zu einem Eintrag.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Konfigurieren Sie das INDEX-Feld nur so, dass XE-Felder angezeigt werden, die innerhalb der Grenzen liegen
// eines Lesezeichens mit dem Namen "MainBookmark" und dessen "EntryType"-Eigenschaften den Wert "A" haben.
// Sowohl für INDEX- als auch für XE-Felder verwendet die Eigenschaft "EntryType" nur das erste Zeichen ihres Zeichenfolgenwerts.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// Beginnen Sie auf einer neuen Seite das Lesezeichen mit einem Namen, der dem Wert entspricht
// der Eigenschaft "BookmarkName" des INDEX-Felds.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// Das INDEX-Feld nimmt diesen Eintrag auf, da er sich innerhalb des Lesezeichens befindet,
// und sein Eintragstyp stimmt auch mit dem Eintragstyp des INDEX-Felds überein.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Fügen Sie ein XE-Feld ein, das nicht im INDEX erscheint, da die Eintragstypen nicht übereinstimmen.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Lesezeichen beenden und danach ein XE-Feld einfügen.
// Es ist vom gleichen Typ wie das INDEX-Feld, wird aber nicht angezeigt
// da es außerhalb der Grenzen des Lesezeichens liegt.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Zeigt, wie ein INDEX-Feld mithilfe von XE-Feldern mit Einträgen gefüllt und sein Erscheinungsbild geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das einen Eintrag für jedes im Dokument gefundene XE-Feld anzeigt.
// Jeder Eintrag zeigt den Text-Eigenschaftswert des XE-Felds auf der linken Seite an,
// und die Nummer der Seite, die rechts das XE-Feld enthält.
// Wenn die XE-Felder den gleichen Wert in ihrer "Text"-Eigenschaft haben,
// das Feld INDEX gruppiert sie zu einem Eintrag.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Wenn Sie den Wert dieser Eigenschaft auf "A" setzen, werden alle Einträge nach ihrem Anfangsbuchstaben gruppiert,
// und platzieren Sie diesen Buchstaben in Großbuchstaben über jeder Gruppe.
index.Heading = "A";

// Stellen Sie die vom INDEX-Feld erstellte Tabelle so ein, dass sie sich über 2 Spalten erstreckt.
index.NumberOfColumns = "2";

// Alle Einträge mit Anfangsbuchstaben außerhalb des "ac"-Zeichenbereichs so einstellen, dass sie weggelassen werden.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Diese nächsten beiden XE-Felder werden unter der Überschrift "A" angezeigt,
// mit ihren jeweiligen Textstilen, die auch auf ihre Seitenzahlen angewendet werden.
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

// Die beiden nächsten beiden XE-Felder werden im Inhaltsverzeichnis der INDEX-Felder unter einer "B"- und einer "C"-Überschrift stehen.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// INDEX-Felder sortieren alle Einträge alphabetisch, sodass dieser Eintrag unter "A" mit den anderen beiden angezeigt wird.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Dieser Eintrag erscheint nicht, da er mit dem Buchstaben "D" beginnt,
// die außerhalb des "ac"-Zeichenbereichs liegt, den die LetterRange-Eigenschaft des INDEX-Felds definiert.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)


