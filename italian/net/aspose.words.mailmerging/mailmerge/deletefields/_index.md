---
title: MailMerge.DeleteFields
second_title: Aspose.Words per .NET API Reference
description: MailMerge metodo. Rimuove i campi relativi alla stampa unione dal documento.
type: docs
weight: 170
url: /it/net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

Rimuove i campi relativi alla stampa unione dal documento.

```csharp
public void DeleteFields()
```

### Osservazioni

Questo metodo rimuove i campi MERGEFIELD e NEXT dal documento.

Questo metodo potrebbe essere utile se l'operazione di stampa unione non richiede sempre di compilare tutti i campi del documento. Utilizza questo metodo per rimuovere tutti i campi di stampa unione rimanenti .

### Esempi

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
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)


