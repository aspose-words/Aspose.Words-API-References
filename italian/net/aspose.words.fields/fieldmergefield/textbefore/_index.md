---
title: FieldMergeField.TextBefore
linktitle: TextBefore
articleTitle: TextBefore
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldMergeField TextBefore per personalizzare facilmente l'inserimento del testo prima dei campi, migliorando la chiarezza e la professionalità del tuo documento.
type: docs
weight: 60
url: /it/net/aspose.words.fields/fieldmergefield/textbefore/
---
## FieldMergeField.TextBefore property

Ottiene o imposta il testo da inserire prima del campo se il campo non è vuoto.

```csharp
public string TextBefore { get; set; }
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
