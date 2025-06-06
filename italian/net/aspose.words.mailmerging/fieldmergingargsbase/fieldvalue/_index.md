---
title: FieldMergingArgsBase.FieldValue
linktitle: FieldValue
articleTitle: FieldValue
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldValue di FieldMergingArgsBase. Accedi e modifica facilmente i valori dei campi dalla tua sorgente dati per una gestione avanzata dei dati.
type: docs
weight: 50
url: /it/net/aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/
---
## FieldMergingArgsBase.FieldValue property

Ottiene o imposta il valore del campo dall'origine dati.

```csharp
public object FieldValue { get; set; }
```

## Osservazioni

Questa proprietà contiene un valore che è stato appena selezionato dalla sorgente dati per questo campo dal motore di stampa unione. È anche possibile sostituire il valore impostando la proprietà.

## Esempi

Mostra come modificare i valori ricevuti dai MERGEFIELD durante una stampa unione.

```csharp
public void FieldFormats()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserire alcuni MERGEFIELD con opzioni di formato che modificheranno i valori ricevuti durante una stampa unione.
    builder.InsertField("MERGEFIELD text_Field1 \\* Caps", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD text_Field2 \\* Upper", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD numeric_Field1 \\# 0.0", null);

    builder.Document.MailMerge.FieldMergingCallback = new FieldValueMergingCallback();

    builder.Document.MailMerge.Execute(
        new string[] { "text_Field1", "text_Field2", "numeric_Field1" },
        new object[] { "Field 1", "Field 2", 10 });
    string t = doc.GetText().Trim();
    Assert.AreEqual("Merge Value For \"Text_Field1\": Field 1, MERGE VALUE FOR \"TEXT_FIELD2\": FIELD 2, 10000.0", doc.GetText().Trim());
}

/// <summary>
/// Modifica i valori ricevuti dai MERGEFIELD durante una stampa unione.
/// Il nome di un MERGEFIELD deve avere un prefisso affinché questo callback abbia effetto sul suo valore.
/// </summary>
private class FieldValueMergingCallback : IFieldMergingCallback
{
    /// <summary>
    /// Chiamato quando una stampa unione unisce i dati in un MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs e)
    {
        if (e.FieldName.StartsWith("text_"))
            e.FieldValue = $"Merge value for \"{e.FieldName}\": {(string)e.FieldValue}";
        else if (e.FieldName.StartsWith("numeric_"))
            e.FieldValue = (int)e.FieldValue * 1000;
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        // Non fare nulla.
    }
}
```

### Guarda anche

* class [FieldMergingArgsBase](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
