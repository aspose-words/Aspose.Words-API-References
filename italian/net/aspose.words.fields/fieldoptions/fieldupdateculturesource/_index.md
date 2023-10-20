---
title: FieldOptions.FieldUpdateCultureSource
linktitle: FieldUpdateCultureSource
articleTitle: FieldUpdateCultureSource
second_title: Aspose.Words per .NET
description: FieldOptions FieldUpdateCultureSource proprietà. Specifica le impostazioni cultura da utilizzare per formattare il risultato del campo in C#.
type: docs
weight: 110
url: /it/net/aspose.words.fields/fieldoptions/fieldupdateculturesource/
---
## FieldOptions.FieldUpdateCultureSource property

Specifica le impostazioni cultura da utilizzare per formattare il risultato del campo.

```csharp
public FieldUpdateCultureSource FieldUpdateCultureSource { get; set; }
```

## Osservazioni

Per impostazione predefinita, viene utilizzata la lingua del thread corrente.

L'impostazione influisce solo sui campi data/ora con cambio formato \\@.

## Esempi

Mostra come specificare l'origine delle impostazioni cultura utilizzate per la formattazione della data durante un aggiornamento di campo o una stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci due campi di unione con la locale tedesca.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Imposta la lingua corrente sull'inglese americano dopo aver preservato il valore originale in una variabile.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Questa unione utilizzerà la lingua del thread corrente per formattare la data, inglese americano.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Configura la successiva unione per ricavare il valore della lingua dal codice di campo. Il valore di quella cultura sarà tedesco.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Il primo risultato dell'unione contiene una data formattata in inglese, mentre il secondo è in tedesco.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Ripristina la lingua originale del thread.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Guarda anche

* enum [FieldUpdateCultureSource](../../fieldupdateculturesource/)
* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
