---
title: StructuredDocumentTag.DateDisplayLocale
linktitle: DateDisplayLocale
articleTitle: DateDisplayLocale
second_title: Aspose.Words per .NET
description: StructuredDocumentTag DateDisplayLocale proprietà. Permette di impostare/ottenere il formato della lingua per la data visualizzata in questoSDT  in C#.
type: docs
weight: 100
url: /it/net/aspose.words.markup/structureddocumenttag/datedisplaylocale/
---
## StructuredDocumentTag.DateDisplayLocale property

Permette di impostare/ottenere il formato della lingua per la data visualizzata in questo**SDT** .

```csharp
public int DateDisplayLocale { get; set; }
```

## Osservazioni

L'accesso a questa proprietà funzionerà solo perDate Tipo SDT.

Per tutti gli altri tipi di SDT si verificherà un'eccezione.

## Esempi

Mostra come richiedere all'utente di inserire una data con un tag di documento strutturato.

```csharp
Document doc = new Document();

// Inserisci un tag di documento strutturato che richiede all'utente di inserire una data.
// In Microsoft Word, questo elemento è noto come "controllo contenuto selezione data".
// Quando si fa clic sulla freccia all'estremità destra di questo tag in Microsoft Word,
// vedremo un popup sotto forma di calendario cliccabile.
// Possiamo usare quel popup per selezionare una data che verrà visualizzata dal tag.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Visualizza la data, secondo la locale araba dell'Arabia Saudita.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Imposta il formato con cui visualizzare la data.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Visualizza la data secondo il calendario Hijri.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Prima che l'utente scelga una data in Microsoft Word, il tag visualizzerà il testo "Fare clic qui per inserire una data.".
// In base al calendario del tag, imposta la proprietà "FullDate" per fare in modo che il tag visualizzi una data predefinita.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Guarda anche

* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
