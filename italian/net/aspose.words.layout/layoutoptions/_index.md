---
title: LayoutOptions Class
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.Layout.LayoutOptions per ottimizzare il controllo del layout dei documenti, migliorando la tua esperienza di elaborazione testi con opzioni di personalizzazione flessibili.
type: docs
weight: 3800
url: /it/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

Contiene le opzioni che consentono di controllare il processo di layout del documento.

Per saperne di più, visita il[Conversione in formato a pagina fissa](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) articolo di documentazione.

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
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | Ottiene o imposta[`IPageLayoutCallback`](../ipagelayoutcallback/) implementazione utilizzata dal modello di layout di pagina. |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | Ottiene o imposta il modo in cui vengono visualizzati i commenti. Il valore predefinito è ShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | Ottiene o imposta la modalità di comportamento per il calcolo dei numeri di pagina quando una sezione continua riavvia la numerazione delle pagine. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | Ottiene o imposta l'indicazione se l'opzione di compatibilità "Usa le metriche della stampante per disporre il documento" viene ignorata. Il valore predefinito è`VERO` . |
| [KeepOriginalFontMetrics](../../aspose.words.layout/layoutoptions/keeporiginalfontmetrics/) { get; set; } | Ottiene o imposta un'indicazione se le metriche del font originale devono essere utilizzate dopo la sostituzione del font. Il valore predefinito è`VERO` . |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | Ottiene le opzioni di revisione. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | Ottiene o imposta l'indicazione se il testo nascosto nel documento viene renderizzato. Il valore predefinito è`falso` . |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | Ottiene o imposta l'indicazione se i segni di paragrafo sono renderizzati. Il valore predefinito è`falso` . |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | Ottiene o imposta[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) implementazione utilizzata per le funzionalità di rendering di tipografia avanzata. |

## Osservazioni

Non creare istanze di questa classe direttamente. Usa il[`LayoutOptions`](../../aspose.words/document/layoutoptions/) proprietà per accedere alle opzioni di layout per questo documento.

Nota che dopo aver modificato una qualsiasi delle opzioni presenti in questa classe,[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) Per applicare le opzioni modificate al layout, è necessario chiamare method .

## Esempi

Mostra come nascondere il testo in un documento di output renderizzato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Inserisce il testo nascosto, quindi specifica se desideriamo ometterlo dal documento renderizzato.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

Mostra come visualizzare i segni di paragrafo in un documento di output renderizzato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Aggiungi alcuni paragrafi, quindi abilita i segni di paragrafo per mostrare la fine dei paragrafi
// con un simbolo pilcrow (¶) quando eseguiamo il rendering del documento.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Mostra come modificare l'aspetto delle revisioni in un documento di output renderizzato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una revisione, quindi cambia il colore di tutte le revisioni in verde.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Rimuovi la barra che appare a sinistra di ogni riga rivista.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout/)
* assemblea [Aspose.Words](../../)
