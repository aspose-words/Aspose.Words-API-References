---
title: FieldChar.GetField
linktitle: GetField
articleTitle: GetField
second_title: Aspose.Words per .NET
description: Scopri il metodo GetField in FieldChar, recupera senza sforzo i campi per una gestione ottimale dei dati e prestazioni migliorate nelle tue applicazioni.
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldchar/getfield/
---
## FieldChar.GetField method

Restituisce un campo per il campo char.

```csharp
public Field GetField()
```

### Valore di ritorno

Un campo per il campo char.

## Osservazioni

Un nuovo[`Field`](../../field/) l'oggetto viene creato ogni volta che viene chiamato il metodo.

## Esempi

Mostra come lavorare con un nodo FieldStart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// Recupera l'oggetto facciata che rappresenta il campo nel documento.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Aggiorna il campo per mostrare la data corrente.
field.Update();
```

### Guarda anche

* class [Field](../../field/)
* class [FieldChar](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
