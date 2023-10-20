---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: Aspose.Words per .NET
description: FieldStart FieldData proprietà. Ottiene i dati del campo personalizzato associati al campo in C#.
type: docs
weight: 10
url: /it/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

Ottiene i dati del campo personalizzato associati al campo.

```csharp
public byte[] FieldData { get; }
```

## Esempi

Mostra come ottenere i dati associati al campo.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.Default.GetString(field.Start.FieldData));
```

### Guarda anche

* class [FieldStart](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
