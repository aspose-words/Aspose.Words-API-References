---
title: FieldIndex.SequenceSeparator
linktitle: SequenceSeparator
articleTitle: SequenceSeparator
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldIndex SequenceSeparator-Eigenschaft und verwalten Sie Zeichenfolgen zum Trennen von Sequenz- und Seitenzahlen in Ihren Anwendungen ganz einfach.
type: docs
weight: 160
url: /de/net/aspose.words.fields/fieldindex/sequenceseparator/
---
## FieldIndex.SequenceSeparator property

Ruft die Zeichenfolge ab oder legt sie fest, die zum Trennen von Sequenznummern und Seitenzahlen verwendet wird.

```csharp
public string SequenceSeparator { get; set; }
```

## Beispiele

Zeigt, wie ein Dokument durch die Kombination von INDEX- und SEQ-Feldern in Teile aufgeteilt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt auf der linken Seite den Text-Eigenschaftswert des XE-Felds an,
// und die Nummer der Seite, die rechts das XE-Feld enthält.
// Wenn die XE-Felder den gleichen Wert in ihrer Eigenschaft "Text" haben,
// Das INDEX-Feld gruppiert sie in einem Eintrag.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Benennen Sie in der Eigenschaft SequenceName eine SEQ-Feldsequenz. Jeder Eintrag dieses INDEX-Feldes wird nun auch angezeigt
// die Nummer, auf der sich die Sequenzzählung an der XE-Feldposition befindet, die diesen Eintrag erstellt hat.
index.SequenceName = "MySequence";

// Legen Sie einen Text fest, der die Sequenz- und Seitenzahlen umgibt, um dem Benutzer deren Bedeutung zu erklären.
// Ein mit dieser Konfiguration erstellter Eintrag zeigt als Seitenzahl etwas wie „MySequence bei 1 auf Seite 1“ an.
// PageNumberSeparator und SequenceSeparator dürfen nicht länger als 15 Zeichen sein.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// SEQ-Felder zeigen eine Zählung an, die bei jedem SEQ-Feld erhöht wird.
// Diese Felder verwalten auch separate Zählungen für jede eindeutige benannte Sequenz
// identifiziert durch die Eigenschaft „SequenceIdentifier“ des SEQ-Felds.
// Fügt ein SEQ-Feld ein, das die Sequenz „MySequence“ auf 1 verschiebt.
// Dieses Feld unterscheidet sich nicht vom normalen Dokumenttext. Es wird nicht im Inhaltsverzeichnis eines INDEX-Felds angezeigt.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// Fügen Sie ein XE-Feld ein, das einen Eintrag im INDEX-Feld erstellt.
// Da „MySequence“ auf 1 steht und dieses XE-Feld auf Seite 2 ist, zusammen mit den benutzerdefinierten Trennzeichen, die wir oben definiert haben,
// Der INDEX-Eintrag dieses Felds zeigt auf der linken Seite „Cat“ und auf der rechten Seite „MySequence bei 1 auf Seite 2“ an.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// Fügen Sie einen Seitenumbruch ein und verwenden Sie SEQ-Felder, um „MySequence“ auf 3 zu verschieben.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// Fügen Sie ein XE-Feld mit derselben Texteigenschaft wie oben ein.
// Der INDEX-Eintrag gruppiert XE-Felder mit übereinstimmenden Werten in der Eigenschaft "Text"
// in einen Eintrag, anstatt für jedes XE-Feld einen Eintrag zu erstellen.
// Da wir uns auf Seite 2 mit „MySequence“ bei 3 befinden, wird „, 3 auf Seite 3“ an denselben INDEX-Eintrag wie oben angehängt.
// Der Seitenzahlenteil dieses INDEX-Eintrags zeigt jetzt „MySequence bei 1 auf Seite 2, 3 auf Seite 3“ an.
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// Fügen Sie ein XE-Feld mit einem neuen und eindeutigen Texteigenschaftswert ein.
// Dadurch wird ein neuer Eintrag mit MySequence bei 3 auf Seite 4 hinzugefügt.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Dog";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Sequence.docx");
```

### Siehe auch

* class [FieldIndex](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
