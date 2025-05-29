---
title: FieldToc.PrefixedSequenceIdentifier
linktitle: PrefixedSequenceIdentifier
articleTitle: PrefixedSequenceIdentifier
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldToc PrefixedSequenceIdentifier-Eigenschaft – verwalten Sie Sequenzkennungen effizient und verbessern Sie die Seitenzahl Ihres Eintrags mit eindeutigen Präfixen.
type: docs
weight: 120
url: /de/net/aspose.words.fields/fieldtoc/prefixedsequenceidentifier/
---
## FieldToc.PrefixedSequenceIdentifier property

Ruft die Kennung einer Sequenz ab oder legt sie fest, bei der der Seitenzahl des Eintrags ein Präfix hinzugefügt werden soll.

```csharp
public string PrefixedSequenceIdentifier { get; set; }
```

## Beispiele

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

* class [FieldToc](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
