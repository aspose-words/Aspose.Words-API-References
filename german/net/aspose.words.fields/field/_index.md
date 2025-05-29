---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.Field, Ihren Schlüssel zur Erweiterung von Microsoft Word-Dokumenten mit dynamischen Feldern für verbesserte Funktionalität und Effizienz.
type: docs
weight: 1920
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
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern werden einbezogen. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt die Feldverknüpfung aus. |
| [Update](../../aspose.words.fields/field/update/#update)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Ein Feld in einem Word-Dokument ist eine komplexe Struktur, die aus mehreren Knoten besteht, darunter Feldstart, Feldcode, Feldtrennzeichen, Feldergebnis und Feldende. Felder können verschachtelt sein, umfangreichen Inhalt enthalten und mehrere Absätze oder Abschnitte in einem Dokument umfassen. Die`Field` Die Klasse ist ein „Fassaden“-Objekt, das x000d-Eigenschaften und -Methoden bereitstellt, die es ermöglichen, mit einem Feld als einzelnem Objekt zu arbeiten.

Der[`Start`](./start/) ,[`Separator`](./separator/) Und[`End`](./end/) Eigenschaften verweisen jeweils auf den -Feldstart-, Trenn- und Endknoten des Felds.

Der Inhalt zwischen Feldanfang und Feldtrennzeichen ist der Feldcode. Der Inhalt zwischen dem Feldtrennzeichen und dem Feldende ist das Feldergebnis. Der Feldcode besteht typischerweise aus einem oder mehreren [`Run`](../../aspose.words/run/) Objekte, die Anweisungen angeben. Von der verarbeitenden Anwendung wird erwartet, dass sie den Feldcode ausführt, um das Feldergebnis zu berechnen.

Die Berechnung der Feldergebnisse wird als Feldaktualisierung bezeichnet. Aspose.Words kann die Ergebnisse der meisten Feldtypen genau wie Microsoft Word aktualisieren. Insbesondere berechnet Aspose.Words die Ergebnisse selbst der komplexesten Formelfelder. Um das Ergebnis eines einzelnen Feldes zu berechnen, verwenden Sie die[`Update`](./update/) Methode. Um Felder im gesamten Dokument zu aktualisieren, verwenden Sie[`UpdateFields`](../../aspose.words/document/updatefields/).

Sie können die Klartextversion des Feldcodes erhalten, indem Sie[`GetFieldCode`](./getfieldcode/)method. Sie können die reine Textversion des Feldergebnisses abrufen und festlegen mit der[`Result`](./result/) property. Sowohl der Feldcode als auch das Feldergebnis können komplexe Inhalte enthalten, wie etwa verschachtelte Felder, Absätze, Formen, Tabellen. In diesem Fall möchten Sie möglicherweise direkt mit den Feldknoten arbeiten, wenn Sie mehr Kontrolle benötigen.

Sie erstellen keine Instanzen des`Field` Klasse direkt. Um ein neues Feld zu erstellen, verwenden Sie die[`InsertField`](../../aspose.words/documentbuilder/insertfield/) Verfahren.

## Beispiele

Zeigt, wie Sie mithilfe eines Feldcodes ein Feld in ein Dokument einfügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Diese Überladung der InsertField-Methode aktualisiert eingefügte Felder automatisch.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### Siehe auch

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
