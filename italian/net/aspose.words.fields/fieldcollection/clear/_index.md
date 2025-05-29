---
title: FieldCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words per .NET
description: Cancella senza sforzo tutti i campi dalla tua FieldCollection con il nostro metodo Clear. Semplifica la gestione dei documenti e migliora l'efficienza oggi stesso!
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldcollection/clear/
---
## FieldCollection.Clear method

Rimuove tutti i campi di questa raccolta dal documento e dalla raccolta stessa.

```csharp
public void Clear()
```

## Esempi

Mostra come rimuovere campi da una raccolta di campi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// Di seguito sono riportati quattro modi per rimuovere campi da una raccolta di campi.
// 1 - Ottenere che un campo si rimuova da solo:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Ottenere dalla raccolta la rimozione di un campo che passiamo al suo metodo di rimozione:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Rimuovi un campo da una raccolta in corrispondenza di un indice:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Rimuovi tutti i campi dalla raccolta in una volta sola:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### Guarda anche

* class [FieldCollection](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
