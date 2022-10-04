---
title: FieldSaveDate
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das SAVEDATEFeld.
type: docs
weight: 2200
url: /de/net/aspose.words.fields/fieldsavedate/
---
## FieldSaveDate class

Implementiert das SAVEDATE-Feld.

```csharp
public class FieldSaveDate : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldSaveDate](fieldsavedate/)() | Default_Constructor |

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
| [UseLunarCalendar](../../aspose.words.fields/fieldsavedate/uselunarcalendar/) { get; set; } | Ruft ab oder legt fest, ob der Hijri-Mondkalender oder der hebräische Mondkalender verwendet werden soll. |
| [UseSakaEraCalendar](../../aspose.words.fields/fieldsavedate/usesakaeracalendar/) { get; set; } | Ruft ab oder legt fest, ob der Saka-Ära-Kalender verwendet werden soll. |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fieldsavedate/useumalquracalendar/) { get; set; } | Ruft ab oder legt fest, ob der Um-al-Qura-Kalender verwendet werden soll. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen (oder Feldende, wenn kein Trennzeichen vorhanden ist) zurück. |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines Elternknotens ist, wird sein Elternabsatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben **Null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld Unlink aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Ruft Datum und Uhrzeit der letzten Speicherung des Dokuments ab. Standardmäßig wird der gregorianische Kalender verwendet.

### Beispiele

Zeigt, wie das Feld SAVEDATE verwendet wird, um das Datum/die Uhrzeit des letzten Speichervorgangs des Dokuments anzuzeigen, der mit Microsoft Word durchgeführt wurde.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// Wir können das Feld SAVEDATE verwenden, um das Datum und die Uhrzeit des letzten Speichervorgangs im Dokument anzuzeigen.
// Der Speichervorgang, auf den sich diese Felder beziehen, ist das manuelle Speichern in einer Anwendung wie Microsoft Word,
// nicht die Save-Methode des Dokuments.
// Nachfolgend sind drei verschiedene Kalendertypen aufgeführt, nach denen das SAVEDATE-Feld das Datum/die Uhrzeit anzeigen kann.
// 1 - Islamischer Mondkalender:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - Umm al-Qura Kalender:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - Indischer Nationalkalender:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// Die SAVEDATE-Felder beziehen ihre Datums-/Uhrzeitwerte aus der integrierten LastSavedTime-Eigenschaft.
// Die Save-Methode des Dokuments aktualisiert diesen Wert nicht, aber wir können ihn trotzdem manuell aktualisieren.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
