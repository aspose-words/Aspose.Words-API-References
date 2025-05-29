---
title: FieldChar.FieldType
linktitle: FieldType
articleTitle: FieldType
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldType di FieldChar, che rivela il tipo di campo, migliorando la gestione dei dati e l'efficienza della programmazione. Scopri di più ora!
type: docs
weight: 10
url: /it/net/aspose.words.fields/fieldchar/fieldtype/
---
## FieldChar.FieldType property

Restituisce il tipo del campo.

```csharp
public FieldType FieldType { get; }
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

* enum [FieldType](../../fieldtype/)
* class [FieldChar](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
