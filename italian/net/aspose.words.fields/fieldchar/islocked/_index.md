---
title: FieldChar.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldChar IsLocked e controlla facilmente il ricalcolo dei campi. Migliora l'accuratezza e l'efficienza del tuo documento oggi stesso!
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldchar/islocked/
---
## FieldChar.IsLocked property

Ottiene o imposta se il campo padre è bloccato (non dovrebbe ricalcolare il suo risultato).

```csharp
public bool IsLocked { get; set; }
```

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

* class [FieldChar](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
