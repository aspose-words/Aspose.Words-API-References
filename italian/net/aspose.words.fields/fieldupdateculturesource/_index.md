---
title: FieldUpdateCultureSource Enum
linktitle: FieldUpdateCultureSource
articleTitle: FieldUpdateCultureSource
second_title: Aspose.Words per .NET
description: Aspose.Words.Fields.FieldUpdateCultureSource enum. Indica quale lingua utilizzare durante laggiornamento del campo in C#.
type: docs
weight: 2560
url: /it/net/aspose.words.fields/fieldupdateculturesource/
---
## FieldUpdateCultureSource enumeration

Indica quale lingua utilizzare durante l'aggiornamento del campo.

```csharp
public enum FieldUpdateCultureSource
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| CurrentThread | `0` | La lingua del thread di esecuzione corrente viene utilizzata per aggiornare i campi. |
| FieldCode | `1` | Viene utilizzata la lingua specificata nelle proprietà di formattazione del campo tramite l'impostazione della lingua. |

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

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
