---
title: MailMerge.DeleteFields
linktitle: DeleteFields
articleTitle: DeleteFields
second_title: Aspose.Words per .NET
description: Ottimizza senza sforzo i tuoi documenti con il metodo MailMerge DeleteFields, rimuovendo i campi di unione di posta non necessari per ottenere risultati più puliti e professionali.
type: docs
weight: 170
url: /it/net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

Rimuove i campi relativi alla stampa unione dal documento.

```csharp
public void DeleteFields()
```

## Osservazioni

Questo metodo rimuove i campi MERGEFIELD e NEXT dal documento.

Questo metodo potrebbe essere utile se l'operazione di stampa unione non richiede sempre per popolare tutti i campi del documento. Utilizzare questo metodo per rimuovere tutti i restanti campi di stampa unione.

## Esempi

Mostra come eliminare tutti i MERGEFIELD da un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.Writeln(",");
builder.Writeln("Greetings!");

Assert.AreEqual(
    "Dear \u0013 MERGEFIELD FirstName \u0014«FirstName»\u0015 \u0013 MERGEFIELD LastName \u0014«LastName»\u0015,\rGreetings!", 
    doc.GetText().Trim());

doc.MailMerge.DeleteFields();

Assert.AreEqual("Dear  ,\rGreetings!", doc.GetText().Trim());
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
