---
title: FieldSeq.SequenceIdentifier
second_title: Aspose.Words für .NET-API-Referenz
description: FieldSeq eigendom. Ermittelt oder setzt den Namen der der zu nummerierenden Artikelserie zugeordnet ist.
type: docs
weight: 60
url: /de/net/aspose.words.fields/fieldseq/sequenceidentifier/
---
## FieldSeq.SequenceIdentifier property

Ermittelt oder setzt den Namen, der der zu nummerierenden Artikelserie zugeordnet ist.

```csharp
public string SequenceIdentifier { get; set; }
```

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

* class [FieldSeq](../)
* namensraum [Aspose.Words.Fields](../../fieldseq/)
* Montage [Aspose.Words](../../../)


