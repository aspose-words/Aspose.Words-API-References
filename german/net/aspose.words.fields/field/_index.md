---
title: Field
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt ein Microsoft WordDokumentfeld dar.
type: docs
weight: 1360
url: /de/net/aspose.words.fields/field/
---
## Field class

Stellt ein Microsoft Word-Dokumentfeld dar.

```csharp
public class Field
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | erhält a[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen (oder Feldende, wenn kein Trennzeichen vorhanden ist) zurück. |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines Elternknotens ist, wird sein Elternabsatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben **Null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld Unlink aus. |
| [Update](../../aspose.words.fields/field/update/#update)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/#update_1)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Ein Feld in einem Word-Dokument ist eine komplexe Struktur, die aus mehreren Knoten besteht, die Feldanfang, Feldcode, Feldtrenner, Feldergebnis und Feldende enthalten. Felder können verschachtelt sein, umfangreiche Inhalte enthalten und mehrere Absätze oder Abschnitte in einem Dokument überspannen . Das`Field`Klasse ist ein "Fassaden"-Objekt, das Eigenschaften und Methoden bereitstellt, die es ermöglichen, mit einem Feld als einzelnes Objekt zu arbeiten.

Das[`Start`](./start/) ,[`Separator`](./separator/) und[`End`](./end/) -Eigenschaften zeigen jeweils auf den -Feldstart-, -separator- und -endknoten des Felds.

Der Inhalt zwischen Feldanfang und Trennzeichen ist der Feldcode. Der Inhalt zwischen dem Feldtrenner und dem Feldende ist das Feldergebnis. Der Feldcode besteht normalerweise aus einem oder mehreren [`Run`](../../aspose.words/run/) Objekte, die Anweisungen angeben. Von der verarbeitenden Anwendung wird erwartet, dass sie den Feldcode ausführt , um das Feldergebnis zu berechnen.

Der Prozess der Berechnung von Feldergebnissen wird als Feldaktualisierung bezeichnet. Aspose.Words kann field -Ergebnisse der meisten Feldtypen genauso aktualisieren wie Microsoft Word es tut. Am bemerkenswertesten ist, dass Aspose.Words Ergebnisse selbst der komplexesten Formelfelder berechnen kann. Um das field -Ergebnis eines einzelnen Felds zu berechnen, verwenden Sie die[`Update`](./update/) Methode. Um Felder im gesamten document zu aktualisieren, verwenden Sie[`UpdateFields`](../../aspose.words/document/updatefields/).

Sie können die Klartextversion des Feldcodes mit der abrufen[`GetFieldCode`](./getfieldcode/) method. Sie können die Nur-Text-Version des Feldergebnisses abrufen und festlegen, indem Sie die verwenden[`Result`](./result/) property. Sowohl der Feldcode als auch das Feldergebnis können komplexe Inhalte enthalten, wie z. B. verschachtelte Felder, Absätze, Formen, Tabellen, und in diesem Fall möchten Sie möglicherweise direkt mit den Feldknoten arbeiten, wenn Sie mehr Kontrolle benötigen.

Sie erstellen keine Instanzen von`Field` Klasse direkt. Um ein neues Feld zu erstellen, verwenden Sie die[`InsertField`](../../aspose.words/documentbuilder/insertfield/) Methode.

### Beispiele

Zeigt, wie ein Feld mithilfe eines Feldcodes in ein Dokument eingefügt wird.

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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
