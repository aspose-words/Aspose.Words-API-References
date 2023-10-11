---
title: FieldIndex.SequenceName
second_title: Aspose.Words für .NET-API-Referenz
description: FieldIndex eigendom. Ruft den Namen einer Sequenz ab oder legt diesen fest deren Nummer in der Seitenzahl enthalten ist.
type: docs
weight: 150
url: /de/net/aspose.words.fields/fieldindex/sequencename/
---
## FieldIndex.SequenceName property

Ruft den Namen einer Sequenz ab oder legt diesen fest, deren Nummer in der Seitenzahl enthalten ist.

```csharp
public string SequenceName { get; set; }
```

### Beispiele

Zeigt, wie ein Dokument durch Kombinieren von INDEX- und SEQ-Feldern in Teile aufgeteilt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das einen Eintrag für jedes im Dokument gefundene XE-Feld anzeigt.
// Jeder Eintrag zeigt den Text-Eigenschaftswert des XE-Felds auf der linken Seite an.
// und die Nummer der Seite, die rechts das XE-Feld enthält.
// Wenn die XE-Felder in ihrer Eigenschaft „Text“ den gleichen Wert haben,
// Das INDEX-Feld gruppiert sie in einem Eintrag.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Benennen Sie in der Eigenschaft „SequenceName“ eine SEQ-Feldsequenz. Jeder Eintrag dieses INDEX-Feldes wird nun auch angezeigt
// die Nummer, auf der sich die Sequenzzählung an der XE-Feldposition befindet, die diesen Eintrag erstellt hat.
index.SequenceName = "MySequence";

// Legen Sie Text fest, der die Reihenfolge und die Seitenzahlen umgibt, um dem Benutzer deren Bedeutung zu erklären.
// Ein mit dieser Konfiguration erstellter Eintrag zeigt an seiner Seitenzahl etwa „MySequence at 1 on page 1“ an.
// PageNumberSeparator und SequenceSeparator dürfen nicht länger als 15 Zeichen sein.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// SEQ-Felder zeigen einen Zähler an, der bei jedem SEQ-Feld erhöht wird.
// Diese Felder verwalten auch separate Zählwerte für jede eindeutig benannte Sequenz
// identifiziert durch die Eigenschaft „SequenceIdentifier“ des SEQ-Felds.
// Ein SEQ-Feld einfügen, das die „MySequence“-Sequenz auf 1 verschiebt.
// Dieses Feld unterscheidet sich nicht vom normalen Dokumenttext. Es erscheint nicht im Inhaltsverzeichnis eines INDEX-Felds.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// Ein XE-Feld einfügen, das einen Eintrag im INDEX-Feld erstellt.
// Da „MySequence“ den Wert 1 hat und sich dieses XE-Feld zusammen mit den oben definierten benutzerdefinierten Trennzeichen auf Seite 2 befindet,
// Der INDEX-Eintrag dieses Feldes zeigt „Cat“ auf der linken Seite und „MySequence at 1 on page 2“ auf der rechten Seite an.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// Einen Seitenumbruch einfügen und SEQ-Felder verwenden, um „MySequence“ auf 3 zu erhöhen.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// Ein XE-Feld mit derselben Text-Eigenschaft wie oben einfügen.
// Der INDEX-Eintrag gruppiert XE-Felder mit übereinstimmenden Werten in der Eigenschaft „Text“.
// in einen Eintrag, anstatt für jedes XE-Feld einen Eintrag vorzunehmen.
// Da wir uns auf Seite 2 mit „MySequence“ bei 3 befinden, wird „, 3 auf Seite 3“ an denselben INDEX-Eintrag wie oben angehängt.
// Der Seitenzahlteil dieses INDEX-Eintrags zeigt jetzt „MySequence at 1 on page 2, 3 on page 3“ an.
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// Ein XE-Feld mit einem neuen und eindeutigen Text-Eigenschaftswert einfügen.
// Dadurch wird ein neuer Eintrag hinzugefügt, mit MySequence bei 3 auf Seite 4.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Dog";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Sequence.docx");
```

### Siehe auch

* class [FieldIndex](../)
* namensraum [Aspose.Words.Fields](../../fieldindex/)
* Montage [Aspose.Words](../../../)


