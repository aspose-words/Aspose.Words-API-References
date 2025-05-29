---
title: FieldSeq Class
linktitle: FieldSeq
articleTitle: FieldSeq
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.Fields.FieldSeq-Klasse für die nahtlose Implementierung von SEQ-Feldern. Verbessern Sie Ihre Dokumentenautomatisierung mit leistungsstarken Funktionen und Flexibilität.
type: docs
weight: 2800
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
| [BookmarkName](../../aspose.words.fields/fieldseq/bookmarkname/) { get; set; } | Ruft einen Lesezeichennamen ab oder legt ihn fest, der auf ein Element an einer anderen Stelle im Dokument und nicht an der aktuellen Position verweist. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber/) { get; set; } | Ruft ab oder legt fest, ob die nächste Sequenznummer für das angegebene Element eingefügt werden soll. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel/) { get; set; } | Ruft eine Ganzzahl ab oder legt sie fest, die eine Überschriftenebene darstellt, auf die die Sequenznummer zurückgesetzt werden soll. Gibt -1 zurück, wenn die Zahl fehlt. |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber/) { get; set; } | Ruft eine Ganzzahl ab oder legt sie fest, auf die die Sequenznummer zurückgesetzt werden soll. Gibt -1 zurück, wenn die Zahl fehlt. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier/) { get; set; } | Ruft den Namen ab, der der Reihe von Elementen zugewiesen ist, die nummeriert werden sollen, oder legt diesen fest. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

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

Nummeriert Kapitel, Tabellen, Abbildungen und andere benutzerdefinierte Listen von Elementen in einem Dokument fortlaufend.

## Beispiele

Zeigt die Erstellung einer Nummerierung mithilfe von SEQ-Feldern.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// SEQ-Felder zeigen eine Zählung an, die bei jedem SEQ-Feld erhöht wird.
// Diese Felder verwalten auch separate Zählungen für jede eindeutige benannte Sequenz
// identifiziert durch die Eigenschaft „SequenceIdentifier“ des SEQ-Felds.
// Fügen Sie ein SEQ-Feld ein, das den aktuellen Zählwert von „MySequence“ anzeigt,
// nachdem Sie die Eigenschaft „ResetNumber“ verwendet haben, um sie auf 100 zu setzen.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Die nächste Zahl in dieser Sequenz mit einem weiteren SEQ-Feld anzeigen.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// Fügen Sie eine Überschrift der Ebene 1 ein.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Fügen Sie ein weiteres SEQ-Feld aus derselben Sequenz ein und konfigurieren Sie es so, dass die Anzahl bei jeder Überschrift auf 1 zurückgesetzt wird.
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

Zeigt, wie Inhaltsverzeichnis und Sequenzfelder kombiniert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein TOC-Feld kann für jedes im Dokument gefundene SEQ-Feld einen Eintrag in seinem Inhaltsverzeichnis erstellen.
// Jeder Eintrag enthält den Absatz, der das SEQ-Feld enthält,
// und die Nummer der Seite, auf der das Feld erscheint.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Konfigurieren Sie dieses TOC-Feld so, dass es eine SequenceIdentifier-Eigenschaft mit dem Wert „MySequence“ hat.
fieldToc.TableOfFiguresLabel = "MySequence";

// Konfigurieren Sie dieses TOC-Feld so, dass nur SEQ-Felder aufgenommen werden, die sich innerhalb der Grenzen eines Lesezeichens befinden
// mit dem Namen "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// SEQ-Felder zeigen eine Zählung an, die bei jedem SEQ-Feld erhöht wird.
// Diese Felder verwalten auch separate Zählungen für jede eindeutige benannte Sequenz
// identifiziert durch die Eigenschaft „SequenceIdentifier“ des SEQ-Felds.
// Fügen Sie ein SEQ-Feld ein, das eine Sequenzkennung hat, die mit dem Inhaltsverzeichnis übereinstimmt
// TableOfFiguresLabel-Eigenschaft. Dieses Feld erzeugt keinen Eintrag im Inhaltsverzeichnis, da es außerhalb
// die durch „BookmarkName“ angegebenen Grenzen des Lesezeichens.
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// Die Sequenz dieses SEQ-Felds entspricht der Eigenschaft „TableOfFiguresLabel“ des Inhaltsverzeichnisses und liegt innerhalb der Grenzen des Lesezeichens.
// Der Absatz, der dieses Feld enthält, wird im Inhaltsverzeichnis als Eintrag angezeigt.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// Die Sequenz dieses SEQ-Feldes stimmt nicht mit der Eigenschaft „TableOfFiguresLabel“ des Inhaltsverzeichnisses überein.
// und liegt innerhalb der Grenzen des Lesezeichens. Der Absatz wird im Inhaltsverzeichnis nicht als Eintrag angezeigt.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// Die Sequenz dieses SEQ-Felds entspricht der Eigenschaft „TableOfFiguresLabel“ des Inhaltsverzeichnisses und liegt innerhalb der Grenzen des Lesezeichens.
// Dieses Feld verweist auch auf ein anderes Lesezeichen. Der Inhalt dieses Lesezeichens wird im Inhaltsverzeichnis für dieses SEQ-Feld angezeigt.
// Das SEQ-Feld selbst zeigt den Inhalt dieses Lesezeichens nicht an.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Erstellen Sie ein Lesezeichen mit Inhalten, die im Inhaltsverzeichniseintrag angezeigt werden, da das obige SEQ-Feld darauf verweist.
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

Zeigt, wie ein Inhaltsverzeichnisfeld mithilfe von SEQ-Feldern mit Einträgen gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein TOC-Feld kann für jedes im Dokument gefundene SEQ-Feld einen Eintrag in seinem Inhaltsverzeichnis erstellen.
// Jeder Eintrag enthält den Absatz, der das SEQ-Feld enthält, und die Seitennummer, auf der das Feld erscheint.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ-Felder zeigen eine Zählung an, die bei jedem SEQ-Feld erhöht wird.
// Diese Felder verwalten auch separate Zählungen für jede eindeutige benannte Sequenz
// identifiziert durch die Eigenschaft „SequenceIdentifier“ des SEQ-Felds.
// Verwenden Sie die Eigenschaft „TableOfFiguresLabel“, um eine Hauptsequenz für das Inhaltsverzeichnis zu benennen.
// Jetzt erstellt dieses Inhaltsverzeichnis nur Einträge aus SEQ-Feldern, deren „SequenceIdentifier“ auf „MySequence“ gesetzt ist.
fieldToc.TableOfFiguresLabel = "MySequence";

// Wir können in der Eigenschaft „PrefixedSequenceIdentifier“ eine andere SEQ-Feldsequenz benennen.
    // SEQ-Felder aus dieser Präfixsequenz erstellen keine TOC-Einträge.
// Jeder TOC-Eintrag, der aus einem SEQ-Feld der Hauptsequenz erstellt wird, zeigt jetzt auch die Anzahl an,
// Die Präfixsequenz befindet sich derzeit im SEQ-Feld der Primärsequenz, das den Eintrag vorgenommen hat.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Jeder Inhaltsverzeichniseintrag zeigt die Anzahl der Präfixsequenzen unmittelbar links an
// der Seitenzahl, auf der das SEQ-Feld der Hauptsequenz erscheint.
// Wir können ein benutzerdefiniertes Trennzeichen angeben, das zwischen diesen beiden Zahlen angezeigt wird.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Es gibt zwei Möglichkeiten, SEQ-Felder zum Füllen dieses Inhaltsverzeichnisses zu verwenden.
// 1 - Einfügen eines SEQ-Feldes, das zur Präfixsequenz des Inhaltsverzeichnisses gehört:
// Dieses Feld erhöht die SEQ-Sequenzanzahl für „PrefixSequence“ um 1.
// Da dieses Feld nicht zur Hauptsequenz gehört, identifiziert
// durch die Eigenschaft „TableOfFiguresLabel“ des Inhaltsverzeichnisses wird es nicht als Eintrag angezeigt.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Einfügen eines SEQ-Feldes, das zur Hauptsequenz des Inhaltsverzeichnisses gehört:
// Dieses SEQ-Feld erstellt einen Eintrag im Inhaltsverzeichnis.
// Der Inhaltsverzeichniseintrag enthält den Absatz, in dem sich das SEQ-Feld befindet, und die Nummer der Seite, auf der es erscheint.
// Dieser Eintrag zeigt auch die aktuelle Anzahl der Präfixsequenzen an.
// durch den Wert in der SeqenceSeparator-Eigenschaft des Inhaltsverzeichnisses von der Seitenzahl getrennt.
// Der Zähler "PrefixSequence" steht bei 1, dieses Hauptsequenz-SEQ-Feld befindet sich auf Seite 2,
// und das Trennzeichen ist „>“, daher wird der Eintrag „1>2“ anzeigen.
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Seite einfügen, Präfixsequenz um 2 erhöhen und anschließend ein SEQ-Feld einfügen, um einen TOC-Eintrag zu erstellen.
// Die Präfixsequenz steht jetzt bei 2 und das SEQ-Feld der Hauptsequenz befindet sich auf Seite 3.
// daher wird im Inhaltsverzeichniseintrag als Seitenanzahl „2>3“ angezeigt.
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
