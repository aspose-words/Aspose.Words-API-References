---
title: FieldIndex.RunSubentriesOnSameLine
linktitle: RunSubentriesOnSameLine
articleTitle: RunSubentriesOnSameLine
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldIndex-Eigenschaft „RunSubentriesOnSameLine“, um Untereinträge einfach inline mit Haupteinträgen zu verwalten und so die Datenorganisation zu optimieren.
type: docs
weight: 140
url: /de/net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

Ruft ab oder legt fest, ob Untereinträge in derselben Zeile wie der Haupteintrag ausgeführt werden.

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

## Beispiele

Zeigt, wie mit Untereinträgen in einem INDEX-Feld gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt auf der linken Seite den Text-Eigenschaftswert des XE-Felds an,
// und die Nummer der Seite, die rechts das XE-Feld enthält.
// Der INDEX-Eintrag sammelt alle XE-Felder mit übereinstimmenden Werten in der Eigenschaft "Text"
// in einen Eintrag, anstatt für jedes XE-Feld einen Eintrag zu erstellen.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// XE-Felder mit einer Texteigenschaft, deren Wert zur Überschrift des INDEX-Eintrags wird.
// Wenn dieser Wert zwei durch einen Doppelpunkt getrennte Zeichenfolgensegmente enthält (der INDEX-Eintrag behandelt :) als Trennzeichen,
// Das erste Segment ist die Überschrift und das zweite Segment wird zur Unterüberschrift.
// Das INDEX-Feld gruppiert die Einträge zunächst alphabetisch, dann, wenn es mehrere XE-Felder mit dem gleichen
// Überschriften, das INDEX-Feld unterteilt sie weiter nach den Werten dieser Überschriften.
// Es kann mehrere Untergruppierungsebenen geben, je nachdem, wie oft
// Die Texteigenschaften von XE-Feldern werden wie folgt segmentiert.
// Standardmäßig erstellt eine INDEX-Feldeintragsgruppe für jede Unterüberschrift innerhalb dieser Gruppe eine neue Zeile.
// Wir können das Flag RunSubentriesOnSameLine auf true setzen, um die Überschrift beizubehalten,
// und jede Unterüberschrift für die Gruppe stattdessen in einer Zeile, wodurch das INDEX-Feld kompakter wird.
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// Fügen Sie zwei XE-Felder ein, jedes auf einer neuen Seite und mit der gleichen Überschrift namens „Überschrift 1“,
// die das INDEX-Feld zum Gruppieren verwendet.
// Wenn RunSubentriesOnSameLine falsch ist, erstellt die INDEX-Tabelle drei Zeilen:
// eine Zeile für die Gruppierungsüberschrift „Überschrift 1“ und eine weitere Zeile für jede Unterüberschrift.
// Wenn RunSubentriesOnSameLine wahr ist, dann wird die INDEX-Tabelle eine einzeilige
// Eintrag, der die Überschrift und alle Unterüberschriften umfasst.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 1";

Assert.AreEqual(" XE  \"Heading 1:Subheading 1\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 2";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + $"Field.INDEX.XE.Subheading.docx");
```

### Siehe auch

* class [FieldIndex](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
