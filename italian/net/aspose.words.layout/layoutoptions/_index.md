---
title: Class LayoutOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Layout.LayoutOptions classe. Contiene le opzioni che consentono di controllare il processo di layout del documento.
type: docs
weight: 3350
url: /it/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

Contiene le opzioni che consentono di controllare il processo di layout del documento.

Per saperne di più, visita il[Conversione nel formato a pagina fissa](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) articolo di documentazione.

```csharp
public class LayoutOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [LayoutOptions](layoutoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | Ottiene o imposta[`IPageLayoutCallback`](../ipagelayoutcallback/) implementazione utilizzata dal modello di layout della pagina. |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | Ottiene o imposta il modo in cui vengono visualizzati i commenti. Il valore predefinito èShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | Ottiene o imposta la modalità di comportamento per il calcolo dei numeri di pagina quando una sezione continua riavvia la numerazione delle pagine. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | Ottiene o imposta l'indicazione se l'opzione di compatibilità "Utilizza parametri stampante per impaginare il documento" viene ignorata. L'impostazione predefinita è`VERO` . |
| [KeepOriginalFontMetrics](../../aspose.words.layout/layoutoptions/keeporiginalfontmetrics/) { get; set; } | Ottiene o imposta un'indicazione se la metrica del carattere originale deve essere utilizzata dopo la sostituzione del carattere. L'impostazione predefinita è`VERO` . |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | Ottiene le opzioni di revisione. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | Ottiene o imposta l'indicazione se viene eseguito il rendering del testo nascosto nel documento. L'impostazione predefinita è`falso` . |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | Ottiene o imposta l'indicazione se viene eseguito il rendering dei segni di paragrafo. L'impostazione predefinita è`falso` . |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | Ottiene o imposta[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) implementazione utilizzata per le funzionalità di rendering di tipografia avanzata. |

### Osservazioni

Non crei direttamente istanze di questa classe. Usa il[`LayoutOptions`](../../aspose.words/document/layoutoptions/) proprietà per accedere alle opzioni di layout per questo documento.

Tieni presente che dopo aver modificato una qualsiasi delle opzioni presenti in questa classe,[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) metodo dovrebbe essere chiamato affinché le opzioni modificate vengano applicate al layout.

### Esempi

Mostra come nascondere il testo in un documento di output sottoposto a rendering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Inserisci il testo nascosto, quindi specifica se desideriamo ometterlo da un documento renderizzato.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

Mostra come visualizzare i segni di paragrafo in un documento di output sottoposto a rendering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Aggiungi alcuni paragrafi, quindi abilita i segni di paragrafo per mostrare la fine dei paragrafi
// con il simbolo pilcrow (¶) quando eseguiamo il rendering del documento.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Mostra come modificare l'aspetto delle revisioni in un documento di output sottoposto a rendering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una revisione, quindi cambia il colore di tutte le revisioni in verde.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Rimuove la barra che appare a sinistra di ogni riga modificata.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout/)
* assemblea [Aspose.Words](../../)


