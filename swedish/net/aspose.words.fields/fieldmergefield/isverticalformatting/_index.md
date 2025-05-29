---
title: FieldMergeField.IsVerticalFormatting
linktitle: IsVerticalFormatting
articleTitle: IsVerticalFormatting
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen FieldMergeField IsVerticalFormatting förbättrar textvisningen genom att aktivera teckenkonvertering för vertikal formatering. Optimera din formatering idag!
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldmergefield/isverticalformatting/
---
## FieldMergeField.IsVerticalFormatting property

Hämtar eller anger om teckenkonvertering ska aktiveras för vertikal formatering.

```csharp
public bool IsVerticalFormatting { get; set; }
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

* class [FieldMergeField](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
