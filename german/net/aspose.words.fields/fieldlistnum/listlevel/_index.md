---
title: FieldListNum.ListLevel
second_title: Aspose.Words für .NET-API-Referenz
description: FieldListNum eigendom. Ruft die Ebene in der Liste ab oder legt sie fest und überschreibt dabei das Standardverhalten des Felds.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldlistnum/listlevel/
---
## FieldListNum.ListLevel property

Ruft die Ebene in der Liste ab oder legt sie fest und überschreibt dabei das Standardverhalten des Felds.

```csharp
public string ListLevel { get; set; }
```

### Beispiele

Zeigt, wie Absätze mit LISTNUM-Feldern nummeriert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// LISTNUM-Felder zeigen eine Zahl an, die bei jedem LISTNUM-Feld erhöht wird.
// Diese Felder verfügen auch über eine Vielzahl von Optionen, die es uns ermöglichen, sie zur Emulation nummerierter Listen zu verwenden.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Listen beginnen standardmäßig bei 1 zu zählen, aber wir können diese Zahl auf einen anderen Wert setzen, z. B. 0.
// In diesem Feld wird „0)“ angezeigt.
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // LISTNUM-Felder verwalten separate Zählungen für jede Listenebene.
// Ein LISTNUM-Feld in denselben Absatz wie ein anderes LISTNUM-Feld einfügen
// erhöht die Listenebene anstelle der Anzahl.
// Das nächste Feld setzt die oben begonnene Zählung fort und zeigt auf Listenebene 1 den Wert „1“ an.
builder.InsertField(FieldType.FieldListNum, true);

// Dieses Feld startet eine Zählung auf Listenebene 2. Es wird der Wert „1“ angezeigt.
builder.InsertField(FieldType.FieldListNum, true);

// Dieses Feld startet eine Zählung auf Listenebene 3. Es wird der Wert „1“ angezeigt.
// Unterschiedliche Listenebenen haben unterschiedliche Formatierungen,
// also zeigen diese Felder zusammen den Wert „1)a)i)“ an.
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Das nächste LISTNUM-Feld, das wir einfügen, setzt die Zählung auf Listenebene fort
// dass das vorherige LISTNUM-Feld aktiviert war.
// Mit der Eigenschaft „ListLevel“ können wir zu einer anderen Listenebene springen.
// Wenn dieses LISTNUM-Feld auf Listenebene 3 bleiben würde, würde es „ii)“ anzeigen.
// aber da wir es auf Listenebene 2 verschoben haben, wird die Zählung auf dieser Ebene fortgesetzt und „b)“ angezeigt.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Wir können die ListName-Eigenschaft festlegen, damit das Feld einen anderen AUTONUM-Feldtyp emuliert.
// „NumberDefault“ emuliert AUTONUM, „OutlineDefault“ emuliert AUTONUMOUT,
// und „LegalDefault“ emuliert AUTONUMLGL-Felder.
// Der Listenname „OutlineDefault“ mit 1 als Startnummer führt zur Anzeige von „I.“
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// Der ListName wird nicht aus dem vorherigen Feld übernommen, daher müssen wir ihn für jedes neue Feld festlegen.
// Dieses Feld setzt die Zählung mit dem anderen Listennamen fort und zeigt „II.“ an.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Siehe auch

* class [FieldListNum](../)
* namensraum [Aspose.Words.Fields](../../fieldlistnum/)
* Montage [Aspose.Words](../../../)


