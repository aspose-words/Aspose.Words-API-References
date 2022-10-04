---
title: FieldSeq
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das SEQFeld.
type: docs
weight: 2240
url: /de/net/aspose.words.fields/fieldseq/
---
## FieldSeq class

Implementiert das SEQ-Feld.

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
| [Format](../../aspose.words.fields/field/format/) { get; } | erhält a[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber/) { get; set; } | Ruft ab oder legt fest, ob die nächste Sequenznummer für das angegebene Element eingefügt werden soll. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel/) { get; set; } | Ruft eine ganze Zahl ab oder legt sie fest, die eine Überschriftenebene darstellt, auf die die Sequenznummer zurückgesetzt werden soll. Gibt -1 zurück, wenn die Zahl fehlt. |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber/) { get; set; } | Ruft eine Ganzzahl ab oder legt sie fest, auf die die Sequenznummer zurückgesetzt werden soll. Gibt -1 zurück, wenn die Zahl fehlt. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier/) { get; set; } | Ermittelt oder setzt den Namen, der der zu nummerierenden Artikelserie zugeordnet ist. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

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

Nummeriert fortlaufend Kapitel, Tabellen, Abbildungen und andere benutzerdefinierte Listen von Elementen in einem Dokument.

### Beispiele

Zeigt die Erstellungsnummerierung mithilfe von SEQ-Feldern an.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// SEQ-Felder zeigen einen Zähler an, der sich bei jedem SEQ-Feld erhöht.
// Diese Felder verwalten auch separate Zählwerte für jede eindeutig benannte Sequenz
// identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Felds.
// Fügen Sie ein SEQ-Feld ein, das den aktuellen Zählwert von "MySequence" anzeigt,
// nachdem die Eigenschaft "ResetNumber" verwendet wurde, um sie auf 100 zu setzen.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Zeigt die nächste Nummer in dieser Sequenz mit einem anderen SEQ-Feld an.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// Füge eine Überschrift der Ebene 1 ein.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Fügen Sie ein weiteres SEQ-Feld aus derselben Sequenz ein und konfigurieren Sie es so, dass der Zähler bei jeder Überschrift auf 1 zurückgesetzt wird.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// Die obige Überschrift ist eine Überschrift der Ebene 1, daher wird der Zähler für diese Sequenz auf 1 zurückgesetzt.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Gehe zur nächsten Nummer dieser Sequenz.
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

// Ein TOC-Feld kann einen Eintrag in seinem Inhaltsverzeichnis für jedes im Dokument gefundene SEQ-Feld erstellen.
// Jeder Eintrag enthält den Absatz, der das SEQ-Feld enthält,
// und die Nummer der Seite, auf der das Feld erscheint.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Konfigurieren Sie dieses TOC-Feld so, dass es eine SequenceIdentifier-Eigenschaft mit dem Wert "MySequence" hat.
fieldToc.TableOfFiguresLabel = "MySequence";

// Konfigurieren Sie dieses TOC-Feld so, dass nur SEQ-Felder erfasst werden, die sich innerhalb der Grenzen eines Lesezeichens befinden
// mit dem Namen "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// SEQ-Felder zeigen einen Zähler an, der sich bei jedem SEQ-Feld erhöht.
// Diese Felder verwalten auch separate Zählwerte für jede eindeutig benannte Sequenz
// identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Felds.
// Füge ein SEQ-Feld ein, das eine Sequenzkennung hat, die mit den Inhaltsverzeichnissen übereinstimmt
// TableOfFiguresLabel-Eigenschaft. Dieses Feld erstellt keinen Eintrag im Inhaltsverzeichnis, da es sich außerhalb befindet
// die durch "BookmarkName" bezeichneten Grenzen des Lesezeichens.
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// Die Sequenz dieses SEQ-Felds stimmt mit der Eigenschaft "TableOfFiguresLabel" des Inhaltsverzeichnisses überein und liegt innerhalb der Grenzen des Lesezeichens.
// Der Absatz, der dieses Feld enthält, wird im Inhaltsverzeichnis als Eintrag angezeigt.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// Die Sequenz dieses SEQ-Felds stimmt nicht mit der Eigenschaft "TableOfFiguresLabel" des Inhaltsverzeichnisses überein,
// und liegt innerhalb der Grenzen des Lesezeichens. Sein Absatz wird im Inhaltsverzeichnis nicht als Eintrag angezeigt.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// Die Sequenz dieses SEQ-Felds stimmt mit der Eigenschaft "TableOfFiguresLabel" des Inhaltsverzeichnisses überein und liegt innerhalb der Grenzen des Lesezeichens.
// Dieses Feld verweist auch auf ein anderes Lesezeichen. Der Inhalt dieses Lesezeichens erscheint im TOC-Eintrag für dieses SEQ-Feld.
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

Zeigt, wie ein TOC-Feld mithilfe von SEQ-Feldern mit Einträgen gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein TOC-Feld kann einen Eintrag in seinem Inhaltsverzeichnis für jedes im Dokument gefundene SEQ-Feld erstellen.
// Jeder Eintrag enthält den Absatz, der das SEQ-Feld enthält, und die Seitennummer, auf der das Feld erscheint.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ-Felder zeigen einen Zähler an, der sich bei jedem SEQ-Feld erhöht.
// Diese Felder verwalten auch separate Zählwerte für jede eindeutig benannte Sequenz
// identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Felds.
// Verwenden Sie die Eigenschaft "TableOfFiguresLabel", um eine Hauptsequenz für das Inhaltsverzeichnis zu benennen.
// Jetzt erstellt dieses Inhaltsverzeichnis nur Einträge aus SEQ-Feldern, deren "SequenceIdentifier" auf "MySequence" gesetzt ist.
fieldToc.TableOfFiguresLabel = "MySequence";

// Wir können in der Eigenschaft "PrefixedSequenceIdentifier" eine andere SEQ-Feldsequenz benennen.
 // SEQ-Felder aus dieser Präfixsequenz erstellen keine TOC-Einträge.
// Jeder TOC-Eintrag, der aus einem SEQ-Feld der Hauptsequenz erstellt wurde, zeigt jetzt auch die Anzahl dieser an
// Die Präfixsequenz ist derzeit im SEQ-Feld der Primärsequenz aktiviert, das den Eintrag vorgenommen hat.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Jeder TOC-Eintrag zeigt die Anzahl der Präfixsequenzen unmittelbar links davon an
// der Seitennummer, auf der das SEQ-Feld der Hauptsequenz erscheint.
// Wir können ein benutzerdefiniertes Trennzeichen angeben, das zwischen diesen beiden Zahlen erscheint.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Es gibt zwei Möglichkeiten, SEQ-Felder zu verwenden, um dieses Inhaltsverzeichnis zu füllen.
// 1 - Einfügen eines SEQ-Felds, das zur Präfixsequenz des Inhaltsverzeichnisses gehört:
// Dieses Feld erhöht den SEQ-Sequenzzähler für die "PrefixSequence" um 1.
// Da dieses Feld nicht zur identifizierten Hauptfolge gehört
// durch die Eigenschaft "TableOfFiguresLabel" des Inhaltsverzeichnisses wird es nicht als Eintrag angezeigt.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Einfügen eines SEQ-Felds, das zur Hauptsequenz des Inhaltsverzeichnisses gehört:
// Dieses SEQ-Feld erstellt einen Eintrag im Inhaltsverzeichnis.
// Der TOC-Eintrag enthält den Absatz, in dem sich das SEQ-Feld befindet, und die Nummer der Seite, auf der es erscheint.
// Dieser Eintrag zeigt auch den Zähler an, bei dem sich die Präfixsequenz derzeit befindet,
// getrennt von der Seitenzahl durch den Wert in der Eigenschaft SequenceSeparator des Inhaltsverzeichnisses.
// Der "PrefixSequence"-Zähler ist auf 1, dieses SEQ-Feld der Hauptsequenz befindet sich auf Seite 2,
// und das Trennzeichen ist ">", sodass der Eintrag "1>2" anzeigt.
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Eine Seite einfügen, die Präfixsequenz um 2 vorrücken und ein SEQ-Feld einfügen, um danach einen TOC-Eintrag zu erstellen.
// Die Präfixsequenz ist jetzt bei 2 und das SEQ-Feld der Hauptsequenz befindet sich auf Seite 3,
// Der TOC-Eintrag zeigt also "2>3" bei seiner Seitenzahl an.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
