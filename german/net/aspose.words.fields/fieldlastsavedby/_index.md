---
title: FieldLastSavedBy Class
linktitle: FieldLastSavedBy
articleTitle: FieldLastSavedBy
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldLastSavedBy, um Ihr Dokumentenmanagement mit der Feldfunktion LASTSAVEDBY zu verbessern. Optimieren Sie Ihren Workflow noch heute!
type: docs
weight: 2510
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
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern werden einbezogen. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt die Feldverknüpfung aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Ruft den Namen des Benutzers ab, der das aktuelle Dokument zuletzt geändert und gespeichert hat, wie in der**Zuletzt geändert von** -Eigenschaft der integrierten Dokumenteigenschaften.

## Beispiele

Zeigt, wie das Feld LASTSAVEDBY verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir ein Dokument in Microsoft Word erstellen, enthält die integrierte Eigenschaft „Zuletzt gespeichert von“ den Namen des Benutzers.
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
