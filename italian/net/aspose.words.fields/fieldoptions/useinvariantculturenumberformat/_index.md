---
title: FieldOptions.UseInvariantCultureNumberFormat
linktitle: UseInvariantCultureNumberFormat
articleTitle: UseInvariantCultureNumberFormat
second_title: Aspose.Words per .NET
description: FieldOptions UseInvariantCultureNumberFormat proprietà. Ottiene o imposta il valore che indica che il formato numerico viene analizzato utilizzando impostazioni cultura invarianti o not in C#.
type: docs
weight: 210
url: /it/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

Ottiene o imposta il valore che indica che il formato numerico viene analizzato utilizzando impostazioni cultura invarianti o not

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

## Osservazioni

Quando questa proprietà è impostata su`VERO` , il formato numerico è preso da una cultura invariante.

Quando questa proprietà è impostata su`falso` , il formato del numero viene preso dalla cultura del thread corrente.

Il valore predefinito è`falso`.

## Esempi

Mostra come formattare i numeri in base alle impostazioni cultura invarianti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

 // A volte, i campi potrebbero non formattare correttamente i numeri in determinate culture.
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1234567,89 .     ", field.Result);

// Per risolvere questo problema, potremmo cambiare la cultura dell'intero thread.
// Un altro modo per risolvere questo problema è impostare questo flag,
// che fa in modo che tutti i campi utilizzino la lingua inglese durante la formattazione dei numeri.
// In questo modo possiamo evitare di cambiare la cultura per l'intero thread.
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### Guarda anche

* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
