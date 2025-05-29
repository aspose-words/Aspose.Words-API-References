---
title: SdtDateStorageFormat Enum
linktitle: SdtDateStorageFormat
articleTitle: SdtDateStorageFormat
second_title: Aspose.Words per .NET
description: Scopri come Aspose.Words.Markup.SdtDateStorageFormat migliora la gestione delle date negli SDT, garantendo un'integrazione fluida dei dati XML nei tuoi documenti.
type: docs
weight: 4700
url: /it/net/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enumeration

Specifica come la data per un SDT di data viene archiviata/recuperata quando l'SDT è associato a un nodo XML nell'archivio dati del documento.

```csharp
public enum SdtDateStorageFormat
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Date | `0` | Il valore della data per un SDT di data viene memorizzato come data nel formato standard XML Schema Date. |
| DateTime | `1` | Il valore della data per un SDT di data viene memorizzato come data nel formato standard XML Schema DateTime. |
| Text | `2` | Il valore della data per una data SDT viene memorizzato come testo. |
| Default | `1` | Per impostazione predefinitaDateTime |

## Esempi

Mostra come richiedere all'utente di immettere una data con un tag di documento strutturato.

```csharp
Document doc = new Document();

// Inserire un tag di documento strutturato che richieda all'utente di immettere una data.
// In Microsoft Word, questo elemento è noto come "controllo contenuto selettore data".
// Quando clicchiamo sulla freccia all'estremità destra di questo tag in Microsoft Word,
// vedremo apparire un pop-up sotto forma di calendario cliccabile.
// Possiamo usare quel popup per selezionare una data che verrà visualizzata dal tag.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Visualizza la data in base alle impostazioni locali dell'Arabia Saudita.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Imposta il formato con cui visualizzare la data.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Visualizza la data secondo il calendario Hijri.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Prima che l'utente scelga una data in Microsoft Word, il tag visualizzerà il testo "Fai clic qui per immettere una data".
// In base al calendario del tag, imposta la proprietà "FullDate" per far sì che il tag visualizzi una data predefinita.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
