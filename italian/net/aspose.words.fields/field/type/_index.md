---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: Field Type proprietà. Ottiene il tipo di campo Microsoft Word in C#.
type: docs
weight: 100
url: /it/net/aspose.words.fields/field/type/
---
## Field.Type property

Ottiene il tipo di campo Microsoft Word.

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
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### Guarda anche

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
