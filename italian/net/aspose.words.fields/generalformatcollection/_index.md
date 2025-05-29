---
title: GeneralFormatCollection Class
linktitle: GeneralFormatCollection
articleTitle: GeneralFormatCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.GeneralFormatCollection: una potente raccolta tipizzata per gestire senza sforzo i formati generali nei tuoi documenti.
type: docs
weight: 3060
url: /it/net/aspose.words.fields/generalformatcollection/
---
## GeneralFormatCollection class

Rappresenta una raccolta tipizzata di formati generali.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class GeneralFormatCollection : IEnumerable<GeneralFormat>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.fields/generalformatcollection/count/) { get; } | Ottiene il numero totale di elementi nella raccolta. |
| [Item](../../aspose.words.fields/generalformatcollection/item/) { get; } | Ottiene un formato generale all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.fields/generalformatcollection/add/)(*[GeneralFormat](../generalformat/)*) | Aggiunge un formato generale alla raccolta. |
| [GetEnumerator](../../aspose.words.fields/generalformatcollection/getenumerator/)() | Restituisce un oggetto enumeratore. |
| [Remove](../../aspose.words.fields/generalformatcollection/remove/)(*[GeneralFormat](../generalformat/)*) | Rimuove tutte le occorrenze del formato generale specificato dalla raccolta. |
| [RemoveAt](../../aspose.words.fields/generalformatcollection/removeat/)(*int*) | Rimuove un'occorrenza di formato generale all'indice specificato. |

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

* enum [GeneralFormat](../generalformat/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
