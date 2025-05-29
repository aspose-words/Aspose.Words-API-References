---
title: FieldOptions.LegacyNumberFormat
linktitle: LegacyNumberFormat
articleTitle: LegacyNumberFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldOptions LegacyNumberFormat per abilitare o disabilitare i formati numerici legacy per i campi, migliorando la compatibilità e le prestazioni.
type: docs
weight: 160
url: /it/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

Ottiene o imposta il valore che indica se il formato numerico legacy (precedente ad AW 13.10) per i campi è abilitato o meno.

```csharp
public bool LegacyNumberFormat { get; set; }
```

## Osservazioni

Quando questa proprietà è impostata su`VERO`, il simbolo modello "#" funzionava come in .net: Sostituisce il cancelletto con la cifra corrispondente, se presente; in caso contrario, nella stringa di risultato non appare alcun simbolo.

Quando questa proprietà è impostata su`falso`, il simbolo del modello "#" funziona come MS Word: Questo elemento di formato specifica le cifre necessarie da visualizzare nel risultato. Se il risultato non include una cifra in quella posizione, MS Word visualizza uno spazio. Ad esempio, { = 9 + 6 \# $### } visualizza $ 15.

Il valore predefinito è`falso`.

## Esempi

Mostra come abilitare la formattazione numerica legacy per i campi.

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
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
