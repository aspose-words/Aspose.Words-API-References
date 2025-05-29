---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: Scopri il tipo di campo di Microsoft Word con la nostra proprietà Tipo di campo. Migliora i tuoi documenti con funzionalità di formattazione precisa e contenuti dinamici.
type: docs
weight: 100
url: /it/net/aspose.words.fields/field/type/
---
## Field.Type property

Ottiene il tipo di campo di Microsoft Word.

```csharp
public virtual FieldType Type { get; }
```

## Esempi

Mostra come inserire un campo in un documento utilizzando un codice di campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Questo sovraccarico del metodo InsertField aggiorna automaticamente i campi inseriti.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### Guarda anche

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
