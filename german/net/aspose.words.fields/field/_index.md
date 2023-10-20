---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: Aspose.Words für .NET
description: Aspose.Words.Fields.Field klas. Stellt ein Microsoft WordDokumentfeld dar in C#.
type: docs
weight: 1510
url: /de/net/aspose.words.fields/field/
---
## Field class

Stellt ein Microsoft Word-Dokumentfeld dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class Field
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ruft a ab[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab, der zwischen dem Feldtrennzeichen und dem Feldende liegt, oder legt diesen fest. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`Null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl der Feldcode als auch das Feldergebnis der untergeordneten Felder sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte child seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`Null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld unlink aus. |
| [Update](../../aspose.words.fields/field/update/#update)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Ein Feld in einem Word-Dokument ist eine komplexe Struktur, die aus mehreren Knoten besteht, die Feldanfang, Feldcode, Feldtrennzeichen, Feldergebnis und Feldende umfassen. Felder können verschachtelt sein, umfangreiche Inhalte enthalten und mehrere Absätze oder Abschnitte in einem Dokument umfassen. Der`Field` Die Klasse ist ein „Fassaden“-Objekt, das Eigenschaften und Methoden bereitstellt, die es ermöglichen, mit einem Feld als einzelnes Objekt zu arbeiten.

Der[`Start`](./start/) ,[`Separator`](./separator/) Und[`End`](./end/) Eigenschaften verweisen jeweils auf den Start-, Trenn- und Endknoten des Felds .

Der Inhalt zwischen Feldanfang und Trennzeichen ist der Feldcode. Der Inhalt zwischen dem Feldtrennzeichen the und dem Feldende ist das Feldergebnis. Der Feldcode besteht normalerweise aus einem oder mehreren [`Run`](../../aspose.words/run/) Objekte, die Anweisungen spezifizieren. Von der Verarbeitungsanwendung wird erwartet, dass sie den Feldcode ausführt , um das Feldergebnis zu berechnen.

Der Prozess der Berechnung der Feldergebnisse wird als Feldaktualisierung bezeichnet. Aspose.Words kann field -Ergebnisse der meisten Feldtypen auf genau die gleiche Weise aktualisieren wie Microsoft Word. Vor allem Aspose.Words kann Ergebnisse selbst der komplexesten Formelfelder berechnen. Um das field -Ergebnis eines einzelnen Felds zu berechnen, verwenden Sie die[`Update`](./update/) Methode. Um Felder im gesamten Dokument zu aktualisieren, verwenden Sie [`UpdateFields`](../../aspose.words/document/updatefields/).

Sie können die Nur-Text-Version des Feldcodes mithilfe von abrufen[`GetFieldCode`](./getfieldcode/) method. Sie können die Nur-Text-Version des Feldergebnisses mithilfe von abrufen und festlegen[`Result`](./result/) property. Sowohl der Feldcode als auch das Feldergebnis können komplexe Inhalte enthalten, wie z. B. verschachtelte Felder, Absätze, Formen, Tabellen. In diesem Fall möchten Sie möglicherweise direkt mit den Feldknoten arbeiten, wenn Sie mehr Kontrolle benötigen.

Sie erstellen keine Instanzen davon`Field` Klasse direkt. Um ein neues Feld zu erstellen, verwenden Sie die[`InsertField`](../../aspose.words/documentbuilder/insertfield/) Methode.

## Beispiele

Zeigt, wie man mithilfe eines Feldcodes ein Feld in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Diese Überladung der InsertField-Methode aktualisiert automatisch eingefügte Felder.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### Siehe auch

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
