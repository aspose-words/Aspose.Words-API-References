---
title: FieldPrintDate Class
linktitle: FieldPrintDate
articleTitle: FieldPrintDate
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldPrintDate, um das Feld PRINTDATE mühelos zu implementieren und so die Dokumentenautomatisierung und -effizienz zu verbessern.
type: docs
weight: 2700
url: /de/net/aspose.words.fields/fieldprintdate/
---
## FieldPrintDate class

Implementiert das PRINTDATE-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldPrintDate : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldPrintDate](fieldprintdate/)() | Default_Constructor |

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
| [UseLunarCalendar](../../aspose.words.fields/fieldprintdate/uselunarcalendar/) { get; set; } | Ruft ab oder legt fest, ob der Hijri-Mondkalender oder der hebräische Mondkalender verwendet werden soll. |
| [UseSakaEraCalendar](../../aspose.words.fields/fieldprintdate/usesakaeracalendar/) { get; set; } | Ruft ab oder legt fest, ob der Saka-Ära-Kalender verwendet werden soll. |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fieldprintdate/useumalquracalendar/) { get; set; } | Ruft ab oder legt fest, ob der Um-al-Qura-Kalender verwendet werden soll. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern werden einbezogen. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt die Feldverknüpfung aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Ruft Datum und Uhrzeit des letzten Dokumentdrucks ab. Standardmäßig wird der Gregorianische Kalender verwendet.

## Beispiele

Zeigt gelesene PRINTDATE-Felder an.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// Wenn ein Dokument von einem Drucker gedruckt oder als PDF gedruckt wird (aber nicht als PDF exportiert wird),
// Die PRINTDATE-Felder zeigen Datum und Uhrzeit des Druckvorgangs an.
// Wenn kein Druckvorgang stattgefunden hat, wird in diesen Feldern „0/0/0000“ angezeigt.
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// Nachfolgend sind drei verschiedene Kalendertypen aufgeführt, je nachdem, ob das Feld PRINTDATE
// kann Datum und Uhrzeit des letzten Druckvorgangs anzeigen.
// 1 - Islamischer Mondkalender:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - Umm al-Qura-Kalender:
Assert.True(field.UseUmAlQuraCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\u", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 - Indischer Nationalkalender:
Assert.True(field.UseSakaEraCalendar);
Assert.AreEqual("1/5/1942 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\s", field.GetFieldCode());
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
