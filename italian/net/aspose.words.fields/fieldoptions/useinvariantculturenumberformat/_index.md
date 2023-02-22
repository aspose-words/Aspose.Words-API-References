---
title: FieldOptions.UseInvariantCultureNumberFormat
second_title: Aspose.Words per .NET API Reference
description: FieldOptions proprietà. Ottiene o imposta il valore che indica che il formato del numero viene analizzato utilizzando impostazioni cultura invarianti o meno
type: docs
weight: 190
url: /it/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

Ottiene o imposta il valore che indica che il formato del numero viene analizzato utilizzando impostazioni cultura invarianti o meno

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

### Osservazioni

Quando questa proprietà è impostata su **VERO** , il formato numerico è preso da una cultura invariante.

Quando questa proprietà è impostata su **falso** il formato del numero è preso dalle impostazioni cultura del thread corrente.

Il valore predefinito è **falso**.

### Esempi

Mostra come formattare i numeri in base alle impostazioni cultura invarianti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

// A volte, i campi potrebbero non formattare correttamente i loro numeri in determinate culture. 
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1234567,89 .     ", field.Result);

// Per risolvere questo problema, potremmo cambiare le impostazioni cultura per l'intero thread.
// Un altro modo per risolvere questo problema è impostare questo flag,
// che fa in modo che tutti i campi utilizzino le impostazioni cultura invarianti durante la formattazione dei numeri.
// In questo modo è possibile evitare di modificare la cultura dell'intero thread.
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### Guarda anche

* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldoptions/)
* assemblea [Aspose.Words](../../../)


