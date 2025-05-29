---
title: FieldListNum Class
linktitle: FieldListNum
articleTitle: FieldListNum
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldListNum für die nahtlose Implementierung von LISTNUM-Feldern. Verbessern Sie die Dokumentenautomatisierung noch heute mit leistungsstarken Funktionen!
type: docs
weight: 2530
url: /de/net/aspose.words.fields/fieldlistnum/
---
## FieldListNum class

Implementiert das LISTNUM-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldListNum : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldListNum](fieldlistnum/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [HasListName](../../aspose.words.fields/fieldlistnum/haslistname/) { get; } | Gibt einen Wert zurück, der angibt, ob der Name einer abstrakten Nummerierungsdefinition durch den Code des Felds bereitgestellt wird. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [ListLevel](../../aspose.words.fields/fieldlistnum/listlevel/) { get; set; } | Ruft die Ebene in der Liste ab oder legt sie fest und überschreibt dabei das Standardverhalten des Felds. |
| [ListName](../../aspose.words.fields/fieldlistnum/listname/) { get; set; } | Ruft den Namen der abstrakten Nummerierungsdefinition ab, die für die Nummerierung verwendet wird, oder legt diesen fest. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [StartingNumber](../../aspose.words.fields/fieldlistnum/startingnumber/) { get; set; } | Ruft den Startwert für dieses Feld ab oder legt ihn fest. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern werden einbezogen. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt die Feldverknüpfung aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

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

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
