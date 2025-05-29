---
title: FieldMergeField.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldMergeField Type för att enkelt komma åt fälttyper i Microsoft Word och förbättra dina dokumentautomatiseringsfunktioner.
type: docs
weight: 70
url: /sv/net/aspose.words.fields/fieldmergefield/type/
---
## FieldMergeField.Type property

Hämtar fälttypen Microsoft Word.

```csharp
public override FieldType Type { get; }
```

## Exempel

Visar hur man använder MERGEFIELD-fält för att utföra en dokumentkoppling.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en datatabell som ska användas som datakälla för dokumentkoppling.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Infoga ett MERGEFIELD med en FieldName-egenskap inställd på namnet på en kolumn i datakällan.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// Vi kan lägga till text före och efter värdet som detta fält accepterar när sammanslagningen sker.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());
Assert.AreEqual(FieldType.FieldMergeField, fieldMergeField.Type);

// Infoga ett annat MERGEFIELD-värde för en annan kolumn i datakällan.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### Se även

* enum [FieldType](../../fieldtype/)
* class [FieldMergeField](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
