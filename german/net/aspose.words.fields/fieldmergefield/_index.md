---
title: Class FieldMergeField
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.FieldMergeField klas. Implementiert das MERGEFIELDFeld.
type: docs
weight: 2000
url: /de/net/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class

Implementiert das MERGEFIELD-Feld.

```csharp
public class FieldMergeField : Field
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [FieldName](../../aspose.words.fields/fieldmergefield/fieldname/) { get; set; } | Ruft den Namen eines Datenfelds ab oder setzt ihn. |
| [FieldNameNoPrefix](../../aspose.words.fields/fieldmergefield/fieldnamenoprefix/) { get; } | Gibt nur den Namen des Datenfelds zurück. Jedes Präfix wird auf die Präfixeigenschaft reduziert. |
| [Format](../../aspose.words.fields/field/format/) { get; } | erhält a[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [IsMapped](../../aspose.words.fields/fieldmergefield/ismapped/) { get; set; } | Ruft ab oder legt fest, ob dieses Feld ein zugeordnetes Feld ist. |
| [IsVerticalFormatting](../../aspose.words.fields/fieldmergefield/isverticalformatting/) { get; set; } | Ruft ab oder legt fest, ob die Zeichenkonvertierung für die vertikale Formatierung aktiviert werden soll. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [TextAfter](../../aspose.words.fields/fieldmergefield/textafter/) { get; set; } | Ermittelt oder setzt den Text, der nach dem Feld eingefügt werden soll, wenn das Feld nicht leer ist. |
| [TextBefore](../../aspose.words.fields/fieldmergefield/textbefore/) { get; set; } | Ruft den Text ab oder setzt ihn, der vor dem Feld eingefügt werden soll, wenn das Feld nicht leer ist. |
| override [Type](../../aspose.words.fields/fieldmergefield/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

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

Ruft den Namen eines Datenfelds innerhalb der Zusammenführungszeichen in einem Seriendruck-Hauptdokument ab. Wenn das Hauptdokument mit der ausgewählten Datenquelle zusammengeführt wird, werden Informationen aus dem angegebenen Datenfeld anstelle des Seriendruckfelds eingefügt.

### Beispiele

Zeigt, wie MERGEFIELD-Felder verwendet werden, um einen Seriendruck durchzuführen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie eine Datentabelle, die als Datenquelle für den Seriendruck verwendet werden soll.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Ein MERGEFIELD mit einer FieldName-Eigenschaft einfügen, die auf den Namen einer Spalte in der Datenquelle gesetzt ist.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// Wir können Text vor und nach dem Wert anwenden, den dieses Feld akzeptiert, wenn die Zusammenführung stattfindet.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());

// Ein weiteres MERGEFIELD für eine andere Spalte in der Datenquelle einfügen.
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


