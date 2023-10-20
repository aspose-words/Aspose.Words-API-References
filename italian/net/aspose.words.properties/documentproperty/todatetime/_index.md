---
title: DocumentProperty.ToDateTime
linktitle: ToDateTime
articleTitle: ToDateTime
second_title: Aspose.Words per .NET
description: DocumentProperty ToDateTime metodo. Restituisce il valore della proprietà comeAppuntamento tra UTC in C#.
type: docs
weight: 80
url: /it/net/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty.ToDateTime method

Restituisce il valore della proprietà come**Appuntamento** tra UTC.

```csharp
public DateTime ToDateTime()
```

## Osservazioni

Genera un'eccezione se il tipo di proprietà non lo èDateTime.

Microsoft Word memorizza solo la parte della data (nessuna ora) per le proprietà della data personalizzate.

## Esempi

Mostra come creare una proprietà del documento personalizzata che contiene una data e un'ora.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

Mostra vari metodi di conversione del tipo delle proprietà personalizzate del documento.

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
