---
title: FieldAsk.PromptText
linktitle: PromptText
articleTitle: PromptText
second_title: Aspose.Words per .NET
description: Scopri come gestire facilmente la proprietà PromptText di FieldAsk per personalizzare il titolo della finestra di prompt e migliorare l'esperienza utente.
type: docs
weight: 50
url: /it/net/aspose.words.fields/fieldask/prompttext/
---
## FieldAsk.PromptText property

Ottiene o imposta il testo del prompt (il titolo della finestra del prompt).

```csharp
public string PromptText { get; set; }
```

## Esempi

Mostra come creare un campo ASK e impostarne le proprietà.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserisci un campo in cui verrà inserita la risposta al nostro campo ASK.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // Inserisci il campo ASK e modifica le sue proprietà per fare riferimento al nostro campo REF tramite il nome del segnalibro.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // I campi ASK applicano la risposta predefinita ai rispettivi campi REF durante una stampa unione.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // Possiamo modificare o sovrascrivere la risposta predefinita nei nostri campi ASK con un risponditore di richiesta personalizzato,
    // che si verificherà durante una stampa unione.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Aggiunge del testo all'inizio della risposta predefinita di un campo ASK durante una stampa unione.
/// </summary>
private class MyPromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response from MyPromptRespondent. " + defaultResponse;
    }
}
```

### Guarda anche

* class [FieldAsk](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
