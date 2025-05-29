---
title: FieldMergeField.IsMapped
linktitle: IsMapped
articleTitle: IsMapped
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FieldMergeField IsMapped“, um zugeordnete Felder einfach zu verwalten und so Ihre Datenintegration und Workflow-Effizienz zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldmergefield/ismapped/
---
## FieldMergeField.IsMapped property

Ruft ab oder legt fest, ob dieses Feld ein zugeordnetes Feld ist.

```csharp
public bool IsMapped { get; set; }
```

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

* class [FieldMergeField](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
