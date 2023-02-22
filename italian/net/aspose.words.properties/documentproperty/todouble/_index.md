---
title: DocumentProperty.ToDouble
second_title: Aspose.Words per .NET API Reference
description: DocumentProperty metodo. Restituisce il valore della proprietà come double.
type: docs
weight: 90
url: /it/net/aspose.words.properties/documentproperty/todouble/
---
## DocumentProperty.ToDouble method

Restituisce il valore della proprietà come double.

```csharp
public double ToDouble()
```

### Osservazioni

Genera un'eccezione se il tipo di proprietà non lo èNumber .

### Esempi

Mostra vari metodi di conversione del tipo di proprietà del documento personalizzate.

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
* spazio dei nomi [Aspose.Words.Properties](../../documentproperty/)
* assemblea [Aspose.Words](../../../)


