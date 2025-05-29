---
title: FieldSeq.SequenceIdentifier
linktitle: SequenceIdentifier
articleTitle: SequenceIdentifier
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldSeq SequenceIdentifier-Eigenschaft, um Artikelseriennamen mühelos zu verwalten und anzupassen und so eine effiziente Nummerierung und Organisation zu ermöglichen.
type: docs
weight: 60
url: /de/net/aspose.words.fields/fieldseq/sequenceidentifier/
---
## FieldSeq.SequenceIdentifier property

Ruft den Namen ab, der der Reihe von Elementen zugewiesen ist, die nummeriert werden sollen, oder legt diesen fest.

```csharp
public string SequenceIdentifier { get; set; }
```

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

* class [FieldSeq](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
