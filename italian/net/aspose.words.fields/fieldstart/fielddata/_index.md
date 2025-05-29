---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: Aspose.Words per .NET
description: Sblocca i dati dei campi personalizzati con la proprietà FieldData di FieldStart, migliorando la gestione dei dati e incrementando la produttività senza sforzo.
type: docs
weight: 10
url: /it/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

Ottiene i dati del campo personalizzato associato al campo.

```csharp
public byte[] FieldData { get; }
```

## Esempi

Mostra come ottenere i dati associati al campo.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.UTF8.GetString(field.Start.FieldData));
```

### Guarda anche

* class [FieldStart](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
