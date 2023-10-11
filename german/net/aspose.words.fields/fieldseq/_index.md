---
title: Class FieldSeq
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.FieldSeq klas. Implementiert das SEQFeld.
type: docs
weight: 2390
url: /de/net/aspose.words.fields/fieldseq/
---
## FieldSeq class

Implementiert das SEQ-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldSeq : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldSeq](fieldseq/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldseq/bookmarkname/) { get; set; } | Ruft einen Lesezeichennamen ab oder legt diesen fest, der auf ein Element an einer anderen Stelle im Dokument und nicht an der aktuellen Position verweist. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ruft a ab[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber/) { get; set; } | Ruft ab oder legt fest, ob die nächste Sequenznummer für das angegebene Element eingefügt werden soll. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel/) { get; set; } | Ruft eine Ganzzahl ab oder legt diese fest, die eine Überschriftenebene darstellt, um die Sequenznummer auf zurückzusetzen. Gibt -1 zurück, wenn die Nummer fehlt. |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber/) { get; set; } | Ruft eine Ganzzahl ab, auf die die Sequenznummer zurückgesetzt werden soll, oder legt diese fest. Gibt -1 zurück, wenn die Nummer fehlt. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab, der zwischen dem Feldtrennzeichen und dem Feldende liegt, oder legt diesen fest. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`Null` . |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier/) { get; set; } | Ruft den Namen ab, der der zu nummerierenden Artikelserie zugewiesen ist, oder legt diesen fest. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl der Feldcode als auch das Feldergebnis der untergeordneten Felder sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte child seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`Null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld unlink aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Nummeriert fortlaufend Kapitel, Tabellen, Abbildungen und andere benutzerdefinierte Listen von Elementen in einem Dokument.

### Beispiele

Zeigt die Erstellung einer Nummerierung mithilfe von SEQ-Feldern an.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// SEQ-Felder zeigen einen Zähler an, der bei jedem SEQ-Feld erhöht wird.
// Diese Felder verwalten auch separate Zählwerte für jede eindeutig benannte Sequenz
// identifiziert durch die Eigenschaft „SequenceIdentifier“ des SEQ-Felds.
// Fügen Sie ein SEQ-Feld ein, das den aktuellen Zählwert von „MySequence“ anzeigt.
// nachdem die Eigenschaft „ResetNumber“ verwendet wurde, um sie auf 100 zu setzen.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Zeigt die nächste Zahl in dieser Sequenz mit einem anderen SEQ-Feld an.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// Eine Überschrift der Ebene 1 einfügen.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Ein weiteres SEQ-Feld aus derselben Sequenz einfügen und so konfigurieren, dass die Zählung bei jeder Überschrift auf 1 zurückgesetzt wird.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// Die obige Überschrift ist eine Überschrift der Ebene 1, daher wird der Zähler für diese Sequenz auf 1 zurückgesetzt.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Zur nächsten Nummer dieser Sequenz wechseln.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\n", fieldSeq.GetFieldCode());
Assert.AreEqual("2", fieldSeq.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

Zeigt, wie Inhaltsverzeichnis- und Sequenzfelder kombiniert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein TOC-Feld kann für jedes im Dokument gefundene SEQ-Feld einen Eintrag in seinem Inhaltsverzeichnis erstellen.
// Jeder Eintrag enthält den Absatz, der das SEQ-Feld enthält,
// und die Nummer der Seite, auf der das Feld erscheint.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Konfigurieren Sie dieses TOC-Feld so, dass es eine SequenceIdentifier-Eigenschaft mit dem Wert „MySequence“ hat.
fieldToc.TableOfFiguresLabel = "MySequence";

// Dieses TOC-Feld so konfigurieren, dass es nur SEQ-Felder aufnimmt, die innerhalb der Grenzen eines Lesezeichens liegen
// mit dem Namen „TOCBookmark“.
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// SEQ-Felder zeigen einen Zähler an, der bei jedem SEQ-Feld erhöht wird.
// Diese Felder verwalten auch separate Zählwerte für jede eindeutig benannte Sequenz
// identifiziert durch die Eigenschaft „SequenceIdentifier“ des SEQ-Felds.
// Fügen Sie ein SEQ-Feld ein, das einen Sequenzbezeichner hat, der mit den Inhaltsverzeichnissen übereinstimmt
// TableOfFiguresLabel-Eigenschaft. Dieses Feld erstellt keinen Eintrag im Inhaltsverzeichnis, da es außerhalb liegt
// die durch „BookmarkName“ bezeichneten Grenzen des Lesezeichens.
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// Die Sequenz dieses SEQ-Felds entspricht der „TableOfFiguresLabel“-Eigenschaft des Inhaltsverzeichnisses und liegt innerhalb der Lesezeichengrenzen.
// Der Absatz, der dieses Feld enthält, wird im Inhaltsverzeichnis als Eintrag angezeigt.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// Die Sequenz dieses SEQ-Felds stimmt nicht mit der „TableOfFiguresLabel“-Eigenschaft des Inhaltsverzeichnisses überein.
// und liegt innerhalb der Grenzen des Lesezeichens. Der zugehörige Absatz wird im Inhaltsverzeichnis nicht als Eintrag angezeigt.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// Die Sequenz dieses SEQ-Felds entspricht der „TableOfFiguresLabel“-Eigenschaft des Inhaltsverzeichnisses und liegt innerhalb der Grenzen des Lesezeichens.
// Dieses Feld verweist auch auf ein anderes Lesezeichen. Der Inhalt dieses Lesezeichens wird im TOC-Eintrag für dieses SEQ-Feld angezeigt.
// Das SEQ-Feld selbst zeigt den Inhalt dieses Lesezeichens nicht an.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Erstellen Sie ein Lesezeichen mit Inhalten, die im TOC-Eintrag angezeigt werden, da das obige SEQ-Feld darauf verweist.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
```

Zeigt, wie ein TOC-Feld mithilfe von SEQ-Feldern mit Einträgen gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein TOC-Feld kann für jedes im Dokument gefundene SEQ-Feld einen Eintrag in seinem Inhaltsverzeichnis erstellen.
// Jeder Eintrag enthält den Absatz, der das SEQ-Feld enthält, und die Seitennummer, auf der das Feld erscheint.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ-Felder zeigen einen Zähler an, der bei jedem SEQ-Feld erhöht wird.
// Diese Felder verwalten auch separate Zählwerte für jede eindeutig benannte Sequenz
// identifiziert durch die Eigenschaft „SequenceIdentifier“ des SEQ-Felds.
// Verwenden Sie die Eigenschaft „TableOfFiguresLabel“, um eine Hauptsequenz für das Inhaltsverzeichnis zu benennen.
// Jetzt erstellt dieses Inhaltsverzeichnis nur Einträge aus SEQ-Feldern, deren „SequenceIdentifier“ auf „MySequence“ gesetzt ist.
fieldToc.TableOfFiguresLabel = "MySequence";

// Wir können eine andere SEQ-Feldsequenz in der Eigenschaft „PrefixedSequenceIdentifier“ benennen.
 // SEQ-Felder aus dieser Präfixsequenz erstellen keine TOC-Einträge.
// Jeder TOC-Eintrag, der aus einem SEQ-Feld der Hauptsequenz erstellt wurde, zeigt jetzt auch die Anzahl an
// Die Präfixsequenz ist derzeit im SEQ-Feld der Primärsequenz aktiviert, das den Eintrag vorgenommen hat.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Bei jedem TOC-Eintrag wird die Anzahl der Präfixsequenzen unmittelbar links angezeigt
// der Seitenzahl, auf der das SEQ-Feld der Hauptsequenz erscheint.
// Wir können ein benutzerdefiniertes Trennzeichen angeben, das zwischen diesen beiden Zahlen angezeigt wird.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Es gibt zwei Möglichkeiten, SEQ-Felder zum Füllen dieses Inhaltsverzeichnisses zu verwenden.
// 1 – Einfügen eines SEQ-Feldes, das zur Präfixsequenz des Inhaltsverzeichnisses gehört:
// Dieses Feld erhöht die SEQ-Sequenzanzahl für die „PrefixSequence“ um 1.
// Da dieses Feld nicht zur identifizierten Hauptsequenz gehört
// Durch die Eigenschaft „TableOfFiguresLabel“ des Inhaltsverzeichnisses wird es nicht als Eintrag angezeigt.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 – Einfügen eines SEQ-Feldes, das zur Hauptsequenz des Inhaltsverzeichnisses gehört:
// Dieses SEQ-Feld erstellt einen Eintrag im Inhaltsverzeichnis.
// Der TOC-Eintrag enthält den Absatz, in dem sich das SEQ-Feld befindet, und die Nummer der Seite, auf der es erscheint.
// Dieser Eintrag zeigt auch die Anzahl an, bei der sich die Präfixsequenz derzeit befindet.
// getrennt von der Seitenzahl durch den Wert in der SeqenceSeparator-Eigenschaft des Inhaltsverzeichnisses.
// Der „PrefixSequence“-Zähler ist bei 1, dieses SEQ-Feld der Hauptsequenz befindet sich auf Seite 2,
// und das Trennzeichen ist „>“, daher wird im Eintrag „1>2“ angezeigt.
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Eine Seite einfügen, die Präfixsequenz um 2 erhöhen und ein SEQ-Feld einfügen, um anschließend einen TOC-Eintrag zu erstellen.
// Die Präfixsequenz befindet sich jetzt bei 2 und das SEQ-Feld der Hauptsequenz befindet sich auf Seite 3.
// Daher wird im Inhaltsverzeichniseintrag bei der Seitenzahl „2>3“ angezeigt.
builder.InsertBreak(BreakType.PageBreak);
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
builder.Write("Second TOC entry, MySequence #");
fieldSeq.SequenceIdentifier = "MySequence";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TOC.SEQ.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)


