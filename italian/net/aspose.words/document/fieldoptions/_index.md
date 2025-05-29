---
title: Document.FieldOptions
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words per .NET
description: Esplora la proprietà Document FieldOptions per gestire efficacemente la gestione dei campi. Scopri opzioni uniche per un controllo e una personalizzazione avanzati dei documenti.
type: docs
weight: 130
url: /it/net/aspose.words/document/fieldoptions/
---
## Document.FieldOptions property

Ottiene un[`FieldOptions`](../../../aspose.words.fields/fieldoptions/) oggetto che rappresenta le opzioni per controllare la gestione dei campi nel documento.

```csharp
public FieldOptions FieldOptions { get; }
```

## Esempi

Mostra come specificare l'origine della cultura utilizzata per la formattazione della data durante un aggiornamento di campo o una stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire due campi di unione con impostazioni locali tedesche.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Imposta la cultura corrente su inglese americano dopo aver preservato il valore originale in una variabile.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Questa unione utilizzerà la cultura del thread corrente per formattare la data, inglese (Stati Uniti).
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Configura la prossima unione in modo che il valore della lingua di destinazione derivi dal codice di campo. Il valore di quella lingua sarà tedesco.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Il primo risultato della fusione contiene una data formattata in inglese, mentre il secondo è in tedesco.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Ripristina la cultura originale del thread.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Guarda anche

* class [FieldOptions](../../../aspose.words.fields/fieldoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
