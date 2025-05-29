---
title: Field.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words per .NET
description: Gestisci le proprietà dei risultati dei campi senza sforzo. Accedi o modifica il testo tra i separatori di campo per una gestione semplificata dei dati e una maggiore efficienza.
type: docs
weight: 70
url: /it/net/aspose.words.fields/field/result/
---
## Field.Result property

Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo.

```csharp
public string Result { get; set; }
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

* class [Field](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
