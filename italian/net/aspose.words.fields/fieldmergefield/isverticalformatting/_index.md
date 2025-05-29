---
title: FieldMergeField.IsVerticalFormatting
linktitle: IsVerticalFormatting
articleTitle: IsVerticalFormatting
second_title: Aspose.Words per .NET
description: Scopri come la proprietà IsVerticalFormatting di FieldMergeField migliora la visualizzazione del testo consentendo la conversione dei caratteri per la formattazione verticale. Ottimizza la tua formattazione oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldmergefield/isverticalformatting/
---
## FieldMergeField.IsVerticalFormatting property

Ottiene o imposta se abilitare la conversione dei caratteri per la formattazione verticale.

```csharp
public bool IsVerticalFormatting { get; set; }
```

## Esempi

Mostra come utilizzare i campi MERGEFIELD per eseguire una stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una tabella dati da utilizzare come origine dati per la stampa unione.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Inserire un MERGEFIELD con una proprietà FieldName impostata sul nome di una colonna nell'origine dati.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// Possiamo applicare del testo prima e dopo il valore che questo campo accetta quando avviene l'unione.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());
Assert.AreEqual(FieldType.FieldMergeField, fieldMergeField.Type);

// Inserisce un altro MERGEFIELD per una colonna diversa nell'origine dati.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### Guarda anche

* class [FieldMergeField](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
