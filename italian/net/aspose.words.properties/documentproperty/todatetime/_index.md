---
title: DocumentProperty.ToDateTime
linktitle: ToDateTime
articleTitle: ToDateTime
second_title: Aspose.Words per .NET
description: Converti DocumentProperty in UTC DateTime senza sforzo. Ottieni timestamp precisi e migliora la gestione dei tuoi dati con il nostro metodo affidabile.
type: docs
weight: 80
url: /it/net/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty.ToDateTime method

Restituisce il valore della proprietà come**Data e ora** in UTC.

```csharp
public DateTime ToDateTime()
```

## Osservazioni

Genera un'eccezione se il tipo di proprietà non èDateTime.

Microsoft Word memorizza solo la parte relativa alla data (non l'ora) per le proprietà di data personalizzate.

## Esempi

Mostra come creare una proprietà di documento personalizzata che contiene una data e un'ora.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

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
