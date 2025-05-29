---
title: FieldFillIn.PromptOnceOnMailMerge
linktitle: PromptOnceOnMailMerge
articleTitle: PromptOnceOnMailMerge
second_title: Aspose.Words per .NET
description: Ottimizza la tua stampa unione con la proprietà PromptOnceOnMailMerge. Controlla le risposte degli utenti per una raccolta dati efficiente nei tuoi documenti.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldfillin/promptonceonmailmerge/
---
## FieldFillIn.PromptOnceOnMailMerge property

Ottiene o imposta se la risposta dell'utente deve essere ricevuta una volta per ogni operazione di unione di posta.

```csharp
public bool PromptOnceOnMailMerge { get; set; }
```

## Esempi

Mostra come utilizzare il campo FILLIN per chiedere all'utente una risposta.

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserisci un campo FILLIN. Quando aggiorniamo manualmente questo campo in Microsoft Word,
    // ci chiederà di inserire una risposta. Il campo visualizzerà quindi la risposta come testo.
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // Possiamo anche utilizzare questi campi per chiedere all'utente una risposta univoca per ogni pagina
    // creato durante una stampa unione effettuata tramite Microsoft Word.
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // Se eseguiamo una stampa unione a livello di programmazione, possiamo utilizzare un prompt responder personalizzato
    // per modificare automaticamente le risposte per i campi FILLIN rilevati dalla stampa unione.
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");
}

/// <summary>
/// Aggiunge una riga all'inizio della risposta predefinita di ogni campo FILLIN durante una stampa unione.
/// </summary>
private class PromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response modified by PromptRespondent. " + defaultResponse;
    }
}
```

### Guarda anche

* class [FieldFillIn](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
