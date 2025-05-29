---
title: DocumentProperty.ToDouble
linktitle: ToDouble
articleTitle: ToDouble
second_title: Aspose.Words per .NET
description: Converti i valori di DocumentProperty in double senza sforzo con il metodo ToDouble. Ottieni subito una gestione precisa dei dati per le tue applicazioni!
type: docs
weight: 90
url: /it/net/aspose.words.properties/documentproperty/todouble/
---
## DocumentProperty.ToDouble method

Restituisce il valore della proprietà come double.

```csharp
public double ToDouble()
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
