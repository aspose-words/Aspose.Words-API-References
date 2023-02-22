---
title: StructuredDocumentTag.CalendarType
second_title: Aspose.Words per .NET API Reference
description: StructuredDocumentTag proprietà. Specifica il tipo di calendario per questo SDT . Limpostazione predefinita èDefault
type: docs
weight: 50
url: /it/net/aspose.words.markup/structureddocumenttag/calendartype/
---
## StructuredDocumentTag.CalendarType property

Specifica il tipo di calendario per questo **SDT** . L'impostazione predefinita èDefault

```csharp
public SdtCalendarType CalendarType { get; set; }
```

### Osservazioni

L'accesso a questa proprietà funzionerà solo perDate Tipo SDT.

Per tutti gli altri tipi di SDT si verificherà un'eccezione.

### Esempi

Mostra come richiedere all'utente di inserire una data con un tag documento strutturato.

```csharp
Document doc = new Document();

// Inserisce un tag di documento strutturato che richiede all'utente di inserire una data.
// In Microsoft Word, questo elemento è noto come "Controllo del contenuto del selettore di date".
// Quando facciamo clic sulla freccia all'estremità destra di questo tag in Microsoft Word,
// vedremo un pop-up sotto forma di un calendario cliccabile.
// Possiamo usare quel popup per selezionare una data che il tag visualizzerà.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Visualizza la data, secondo le impostazioni locali dell'arabo saudita.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Imposta il formato con cui visualizzare la data.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Visualizza la data secondo il calendario Hijri.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Prima che l'utente scelga una data in Microsoft Word, il tag visualizzerà il testo "Fai clic qui per inserire una data.".
// In base al calendario del tag, imposta la proprietà "FullDate" per fare in modo che il tag visualizzi una data predefinita.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Guarda anche

* enum [SdtCalendarType](../../sdtcalendartype/)
* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../structureddocumenttag/)
* assemblea [Aspose.Words](../../../)


