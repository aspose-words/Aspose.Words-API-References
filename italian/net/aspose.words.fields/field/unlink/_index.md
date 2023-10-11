---
title: Field.Unlink
second_title: Aspose.Words per .NET API Reference
description: Field metodo. Esegue lo scollegamento del campo.
type: docs
weight: 130
url: /it/net/aspose.words.fields/field/unlink/
---
## Field.Unlink method

Esegue lo scollegamento del campo.

```csharp
public bool Unlink()
```

### Valore di ritorno

`VERO` se il campo è stato scollegato, altrimenti`falso` .

### Osservazioni

Sostituisce il campo con il risultato più recente.

Alcuni campi, come i campi XE (voce indice) e i campi SEQ (sequenza), non possono essere scollegati.

### Esempi

Mostra come scollegare un campo.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");
doc.Range.Fields[1].Unlink();
```

### Guarda anche

* class [Field](../)
* spazio dei nomi [Aspose.Words.Fields](../../field/)
* assemblea [Aspose.Words](../../../)


