---
title: FieldLastSavedBy Class
linktitle: FieldLastSavedBy
articleTitle: FieldLastSavedBy
second_title: Aspose.Words für .NET
description: Aspose.Words.Fields.FieldLastSavedBy klas. Implementiert das Feld LASTSAVEDBY in C#.
type: docs
weight: 2100
url: /de/net/aspose.words.fields/fieldlastsavedby/
---
## FieldLastSavedBy class

Implementiert das Feld LASTSAVEDBY.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldLastSavedBy : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldLastSavedBy](fieldlastsavedby/)() | Default_Constructor |

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
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl der Feldcode als auch das Feldergebnis der untergeordneten Felder sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte child seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`Null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld unlink aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Ruft den Namen des Benutzers ab, der das aktuelle Dokument zuletzt geändert und gespeichert hat, wie im aufgezeichnet**Zuletzt geändert durch** Eigenschaft der integrierten Dokumenteigenschaften.

## Beispiele

Zeigt, wie das Feld LASTSAVEDBY verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir ein Dokument in Microsoft Word erstellen, wird der Name des Benutzers in der integrierten Eigenschaft „Zuletzt gespeichert von“ angezeigt.
 // Wenn wir ein Dokument programmgesteuert erstellen, ist diese Eigenschaft null und wir müssen einen Wert zuweisen.
doc.BuiltInDocumentProperties.LastSavedBy = "John Doe";

// Wir können das Feld LASTSAVEDBY verwenden, um den Wert dieser Eigenschaft im Dokument anzuzeigen.
FieldLastSavedBy field = (FieldLastSavedBy)builder.InsertField(FieldType.FieldLastSavedBy, true);

Assert.AreEqual(" LASTSAVEDBY ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

doc.Save(ArtifactsDir + "Field.LASTSAVEDBY.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
