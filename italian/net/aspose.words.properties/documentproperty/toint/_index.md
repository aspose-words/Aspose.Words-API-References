---
title: DocumentProperty.ToInt
linktitle: ToInt
articleTitle: ToInt
second_title: Aspose.Words per .NET
description: Converti facilmente i valori di DocumentProperty in interi con il metodo ToInt. Sblocca una gestione dati impeccabile per le tue applicazioni!
type: docs
weight: 100
url: /it/net/aspose.words.properties/documentproperty/toint/
---
## DocumentProperty.ToInt method

Restituisce il valore della proprietà come intero.

```csharp
public int ToInt()
```

## Osservazioni

Genera un'eccezione se il tipo di proprietà non èNumber .

## Esempi

Mostra vari metodi di conversione del tipo di proprietà di documenti personalizzati.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

DateTime authDate = DateTime.Today;
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", authDate);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

Assert.AreEqual(true, properties["Authorized"].ToBool());
Assert.AreEqual("John Doe", properties["Authorized By"].ToString());
Assert.AreEqual(authDate, properties["Authorized Date"].ToDateTime());
Assert.AreEqual(1, properties["Authorized Revision"].ToInt());
Assert.AreEqual(123.45d, properties["Authorized Amount"].ToDouble());
```

### Guarda anche

* class [DocumentProperty](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
