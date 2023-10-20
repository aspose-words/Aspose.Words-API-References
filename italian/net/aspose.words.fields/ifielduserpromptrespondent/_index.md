---
title: IFieldUserPromptRespondent Interface
linktitle: IFieldUserPromptRespondent
articleTitle: IFieldUserPromptRespondent
second_title: Aspose.Words per .NET
description: Aspose.Words.Fields.IFieldUserPromptRespondent interfaccia. Rappresenta lintervistato alle richieste dellutente durante laggiornamento del campo in C#.
type: docs
weight: 2740
url: /it/net/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface

Rappresenta l'intervistato alle richieste dell'utente durante l'aggiornamento del campo.

```csharp
public interface IFieldUserPromptRespondent
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Respond](../../aspose.words.fields/ifielduserpromptrespondent/respond/)(*string, string*) | Una volta implementato, restituisce una risposta dall'utente al prompt. La tua implementazione dovrebbe restituire`nullo` per indicare che l'utente non ha risposto al prompt (ovvero l'utente ha premuto il pulsante Annulla nella finestra del prompt). |

## Osservazioni

I campi ASK e FILLIN sono esempi di campi che richiedono all'utente una risposta. Implementa questa interfaccia e assegnala a[`UserPromptRespondent`](../fieldoptions/userpromptrespondent/) proprietà per stabilire l'interazione tra il campo update e l'utente.

## Esempi

Mostra come creare un campo ASK e impostarne le proprietà.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Posiziona un campo in cui verrà inserita la risposta al nostro campo ASK.
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

    // Possiamo modificare o sovrascrivere la risposta predefinita nei nostri campi ASK con un risponditore personalizzato,
    // che si verificherà durante una stampa unione.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// Antepone il testo alla risposta predefinita di un campo ASK durante una stampa unione.
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

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
