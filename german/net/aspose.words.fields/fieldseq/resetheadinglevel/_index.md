---
title: FieldSeq.ResetHeadingLevel
second_title: Aspose.Words für .NET-API-Referenz
description: FieldSeq eigendom. Ruft eine Ganzzahl ab oder legt diese fest die eine Überschriftenebene darstellt um die Sequenznummer auf zurückzusetzen. Gibt 1 zurück wenn die Nummer fehlt.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldseq/resetheadinglevel/
---
## FieldSeq.ResetHeadingLevel property

Ruft eine Ganzzahl ab oder legt diese fest, die eine Überschriftenebene darstellt, um die Sequenznummer auf zurückzusetzen. Gibt -1 zurück, wenn die Nummer fehlt.

```csharp
public string ResetHeadingLevel { get; set; }
```

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

### Siehe auch

* class [FieldSeq](../)
* namensraum [Aspose.Words.Fields](../../fieldseq/)
* Montage [Aspose.Words](../../../)


