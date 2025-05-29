---
title: FieldCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words per .NET
description: Rimuovi senza sforzo campi specifici dal tuo documento con il metodo FieldCollection Remove, semplificando il processo di gestione dei dati.
type: docs
weight: 50
url: /it/net/aspose.words.fields/fieldcollection/remove/
---
## FieldCollection.Remove method

Rimuove il campo specificato da questa raccolta e dal documento.

```csharp
public void Remove(Field field)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| field | Field | Un campo da rimuovere. |

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

* class [Field](../../field/)
* class [FieldCollection](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
