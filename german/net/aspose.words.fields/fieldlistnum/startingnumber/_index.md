---
title: FieldListNum.StartingNumber
linktitle: StartingNumber
articleTitle: StartingNumber
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FieldListNum StartingNumber“, um den Startwert Ihres Felds einfach zu verwalten und so die Datenorganisation und Effizienz zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words.fields/fieldlistnum/startingnumber/
---
## FieldListNum.StartingNumber property

Ruft den Startwert für dieses Feld ab oder legt ihn fest.

```csharp
public string StartingNumber { get; set; }
```

## Beispiele

Zeigt, wie Absätze mit LISTNUM-Feldern nummeriert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// LISTNUM-Felder zeigen eine Zahl an, die bei jedem LISTNUM-Feld erhöht wird.
// Diese Felder verfügen auch über eine Reihe von Optionen, mit denen wir sie zum Emulieren nummerierter Listen verwenden können.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Listen beginnen standardmäßig bei 1 zu zählen, aber wir können diese Zahl auf einen anderen Wert setzen, beispielsweise 0.
// In diesem Feld wird „0)“ angezeigt.
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

// LISTNUM-Felder verwalten separate Zählungen für jede Listenebene.
// Einfügen eines LISTNUM-Felds im selben Absatz wie ein anderes LISTNUM-Feld
// erhöht die Listenebene anstelle der Anzahl.
// Das nächste Feld setzt die oben begonnene Zählung fort und zeigt auf Listenebene 1 einen Wert von „1“ an.
builder.InsertField(FieldType.FieldListNum, true);

// Dieses Feld startet eine Zählung auf Listenebene 2. Es wird der Wert „1“ angezeigt.
builder.InsertField(FieldType.FieldListNum, true);

// Dieses Feld startet eine Zählung auf Listenebene 3. Es wird der Wert „1“ angezeigt.
// Verschiedene Listenebenen haben unterschiedliche Formatierungen,
// Daher wird in diesen Feldern zusammen der Wert „1)a)i)“ angezeigt.
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Das nächste LISTNUM-Feld, das wir einfügen, setzt die Zählung auf Listenebene fort
// auf dem sich das vorherige LISTNUM-Feld befand.
// Wir können die Eigenschaft „ListLevel“ verwenden, um zu einer anderen Listenebene zu springen.
// Wenn dieses LISTNUM-Feld auf Listenebene 3 bliebe, würde es "ii)" anzeigen,
// aber da wir es auf Listenebene 2 verschoben haben, führt es die Zählung auf dieser Ebene fort und zeigt „b)“ an.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Wir können die ListName-Eigenschaft festlegen, damit das Feld einen anderen AUTONUM-Feldtyp emuliert.
// "NumberDefault" emuliert AUTONUM, "OutlineDefault" emuliert AUTONUMOUT,
// und „LegalDefault“ emuliert AUTONUMLGL-Felder.
// Der Listenname „OutlineDefault“ mit 1 als Startzahl führt zur Anzeige von „I.“.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// Der Listenname wird nicht aus dem vorherigen Feld übernommen, daher müssen wir ihn für jedes neue Feld festlegen.
// Dieses Feld führt die Zählung mit dem anderen Listennamen fort und zeigt „II.“ an.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Siehe auch

* class [FieldListNum](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
