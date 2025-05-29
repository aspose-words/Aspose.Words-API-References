---
title: FieldFormat Class
linktitle: FieldFormat
articleTitle: FieldFormat
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldFormat per accedere facilmente ai campi numerici, di data e di ora. Migliora la formattazione dei documenti con potenti funzionalità!
type: docs
weight: 2350
url: /it/net/aspose.words.fields/fieldformat/
---
## FieldFormat class

Fornisce accesso tipizzato alla formattazione numerica, di data e ora e generale del campo.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldFormat
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DateTimeFormat](../../aspose.words.fields/fieldformat/datetimeformat/) { get; set; } | Ottiene o imposta una formattazione applicata al risultato di un campo data e ora. Corrisponde all'opzione \@. |
| [GeneralFormats](../../aspose.words.fields/fieldformat/generalformats/) { get; } | Ottiene una raccolta di formati generali applicati a un risultato numerico, di testo o di qualsiasi campo. Corrisponde agli switch \*. |
| [NumericFormat](../../aspose.words.fields/fieldformat/numericformat/) { get; set; } | Ottiene o imposta una formattazione applicata al risultato di un campo numerico. Corrisponde all'opzione \#. |

## Esempi

Mostra come formattare i risultati dei campi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilizzare un generatore di documenti per inserire un campo che visualizza un risultato senza alcun formato applicato.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Possiamo applicare un formato al risultato di un campo utilizzando le proprietà del campo.
// Di seguito sono riportati tre tipi di formati che possiamo applicare al risultato di un campo.
// 1 - Formato numerico:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Formato data/ora:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - Formato generale:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// Possiamo rimuovere i nostri formati per ripristinare il risultato del campo alla sua forma originale.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
