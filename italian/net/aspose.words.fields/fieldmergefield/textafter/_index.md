---
title: FieldMergeField.TextAfter
linktitle: TextAfter
articleTitle: TextAfter
second_title: Aspose.Words per .NET
description: FieldMergeField TextAfter proprietà. Ottiene o imposta il testo da inserire dopo il campo se il campo non è vuoto in C#.
type: docs
weight: 50
url: /it/net/aspose.words.fields/fieldmergefield/textafter/
---
## FieldMergeField.TextAfter property

Ottiene o imposta il testo da inserire dopo il campo se il campo non è vuoto.

```csharp
public string TextAfter { get; set; }
```

## Esempi

Mostra come utilizzare i campi MERGEFIELD per eseguire una stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una tabella dati da utilizzare come origine dati di stampa unione.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Inserisci un MERGEFIELD con una proprietà FieldName impostata sul nome di una colonna nell'origine dati.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// Possiamo applicare del testo prima e dopo il valore accettato da questo campo quando avviene la fusione.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());

// Inserisci un altro MERGEFIELD per una colonna diversa nell'origine dati.
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
