---
title: FieldCollection.Remove
second_title: Aspose.Words per .NET API Reference
description: FieldCollection metodo. Rimuove il campo specificato da questa raccolta e dal documento.
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

### Esempi

Mostra come rimuovere i campi da una raccolta di campi.

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

// Di seguito sono riportati quattro modi per rimuovere i campi da una raccolta di campi.
// 1 - Ottieni un campo da rimuovere:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Ottieni la raccolta per rimuovere un campo che passiamo al suo metodo di rimozione:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Rimuove un campo da una raccolta in un indice:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Rimuovi tutti i campi dalla raccolta in una volta:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### Guarda anche

* class [Field](../../field/)
* class [FieldCollection](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldcollection/)
* assemblea [Aspose.Words](../../../)


