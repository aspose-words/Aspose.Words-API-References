---
title: FieldMergeField Class
linktitle: FieldMergeField
articleTitle: FieldMergeField
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldMergeField für nahtlose Dokumentenautomatisierung. Verbessern Sie Ihre Workflows mit der leistungsstarken MERGEFIELD-Funktionalität.
type: docs
weight: 2560
url: /de/net/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class

Implementiert das MERGEFIELD-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldMergeField : Field
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [FieldName](../../aspose.words.fields/fieldmergefield/fieldname/) { get; set; } | Ruft den Namen eines Datenfelds ab oder legt ihn fest. |
| [FieldNameNoPrefix](../../aspose.words.fields/fieldmergefield/fieldnamenoprefix/) { get; } | Gibt nur den Namen des Datenfelds zurück. Ein eventuell vorhandenes Präfix wird aus der Präfixeigenschaft entfernt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [IsMapped](../../aspose.words.fields/fieldmergefield/ismapped/) { get; set; } | Ruft ab oder legt fest, ob dieses Feld ein zugeordnetes Feld ist. |
| [IsVerticalFormatting](../../aspose.words.fields/fieldmergefield/isverticalformatting/) { get; set; } | Ruft ab oder legt fest, ob die Zeichenkonvertierung für die vertikale Formatierung aktiviert werden soll. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [TextAfter](../../aspose.words.fields/fieldmergefield/textafter/) { get; set; } | Ruft den Text ab oder legt ihn fest, der nach dem Feld eingefügt werden soll, wenn das Feld nicht leer ist. |
| [TextBefore](../../aspose.words.fields/fieldmergefield/textbefore/) { get; set; } | Ruft den Text ab oder legt ihn fest, der vor dem Feld eingefügt werden soll, wenn das Feld nicht leer ist. |
| override [Type](../../aspose.words.fields/fieldmergefield/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

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

Ruft den Namen eines Datenfelds innerhalb der Seriendruckzeichen in einem Seriendruck-Hauptdokument ab. Wenn das Hauptdokument mit der ausgewählten Datenquelle zusammengeführt wird, werden Informationen aus dem angegebenen Datenfeld anstelle des Seriendruckfelds eingefügt.

## Beispiele

Zeigt, wie MERGEFIELD-Felder zum Ausführen eines Serienbriefs verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie eine Datentabelle, die als Datenquelle für Serienbriefe verwendet werden soll.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Fügen Sie ein MERGEFIELD mit einer FieldName-Eigenschaft ein, die auf den Namen einer Spalte in der Datenquelle festgelegt ist.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// Wir können Text vor und nach dem Wert anwenden, den dieses Feld akzeptiert, wenn die Zusammenführung stattfindet.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());
Assert.AreEqual(FieldType.FieldMergeField, fieldMergeField.Type);

// Fügen Sie ein weiteres MERGEFIELD für eine andere Spalte in der Datenquelle ein.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
