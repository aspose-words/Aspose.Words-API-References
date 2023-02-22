---
title: FieldOptions.LegacyNumberFormat
second_title: Aspose.Words per .NET API Reference
description: FieldOptions proprietà. Ottiene o imposta il valore che indica se il formato numerico legacy precedente a AW 13.10 per i campi è abilitato o meno.
type: docs
weight: 140
url: /it/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

Ottiene o imposta il valore che indica se il formato numerico legacy (precedente a AW 13.10) per i campi è abilitato o meno.

```csharp
public bool LegacyNumberFormat { get; set; }
```

### Osservazioni

Quando questa proprietà è impostata su **VERO**, il simbolo del modello "#" funziona come in .net: Sostituisce il cancelletto con la cifra corrispondente se presente; in caso contrario, nella stringa del risultato non viene visualizzato alcun simbolo.

Quando questa proprietà è impostata su **falso**, il simbolo del modello "#" funziona come MS Word: Questo elemento di formato specifica i posti numerici necessari da visualizzare nel risultato. Se il risultato non include una cifra in quel punto, MS Word visualizza uno spazio. Ad esempio, { = 9 + 6 \# $### } visualizza $ 15.

Il valore predefinito è **falso**.

### Esempi

Mostra come abilitare la formattazione dei numeri legacy per i campi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("= 2 + 3 \\# $##");

Assert.AreEqual("$ 5", field.Result);

doc.FieldOptions.LegacyNumberFormat = true;
field.Update();

Assert.AreEqual("$5", field.Result);
```

### Guarda anche

* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldoptions/)
* assemblea [Aspose.Words](../../../)


