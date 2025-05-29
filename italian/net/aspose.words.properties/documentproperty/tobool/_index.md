---
title: DocumentProperty.ToBool
linktitle: ToBool
articleTitle: ToBool
second_title: Aspose.Words per .NET
description: Scopri il metodo DocumentProperty ToBool che converte in modo efficiente i valori delle proprietà in valori booleani per una gestione dei dati ottimale e una maggiore efficienza di codifica.
type: docs
weight: 60
url: /it/net/aspose.words.properties/documentproperty/tobool/
---
## DocumentProperty.ToBool method

Restituisce il valore della proprietà come bool.

```csharp
public bool ToBool()
```

## Osservazioni

Genera un'eccezione se il tipo di proprietà non èBoolean.

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
