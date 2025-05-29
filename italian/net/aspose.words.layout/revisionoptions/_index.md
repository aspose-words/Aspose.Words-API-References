---
title: RevisionOptions Class
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Layout.RevisionOptions per gestire in modo efficiente le revisioni dei documenti e migliorare il processo di impaginazione per risultati ottimali.
type: docs
weight: 3840
url: /it/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Consente di controllare come vengono gestite le revisioni dei documenti durante il processo di impaginazione.

Per saperne di più, visita il[Conversione in formato a pagina fissa](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) articolo di documentazione.

```csharp
public class RevisionOptions
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Consente di specificare il colore da utilizzare per i commenti. Il valore predefinito èRed . |
| [DeleteCellColor](../../aspose.words.layout/revisionoptions/deletecellcolor/) { get; set; } | Consente di specificare il colore da utilizzare per le celle eliminateDeletion . Il valore predefinito èPink . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Consente di specificare il colore da utilizzare per il contenuto eliminatoDeletion . Il valore predefinito èByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Permette di specificare l'effetto da applicare al contenuto eliminatoDeletion . Il valore predefinito èStrikeThrough |
| [InsertCellColor](../../aspose.words.layout/revisionoptions/insertcellcolor/) { get; set; } | Permette di specificare il colore da utilizzare per le celle inseriteInsertion . Il valore predefinito èBlue . |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Permette di specificare il colore da utilizzare per il contenuto inseritoInsertion . Il valore predefinito èByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Permette di specificare l'effetto da applicare al contenuto inseritoInsertion . Il valore predefinito èUnderline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Consente di specificare le unità di misura per i commenti di revisione. Il valore predefinito èCentimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | Consente di specificare il colore da utilizzare per le aree da cui è stato spostato il contenutoMoving . Il valore predefinito èByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | Consente di specificare l'effetto da applicare alle aree da cui è stato spostato il contenutoMoving . Il valore predefinito èDoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | Consente di specificare il colore da utilizzare per le aree in cui è stato spostato il contenutoMoving . Il valore predefinito èByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | Permette di specificare l'effetto da applicare alle aree in cui è stato spostato il contenutoMoving . Il valore predefinito èDoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Consente di specificare il colore da utilizzare per il contenuto con modifiche delle proprietà di formattazioneFormatChange Il valore predefinito èNoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Consente di specificare l'effetto per le aree di contenuto con modifiche delle proprietà di formattazioneFormatChange Il valore predefinito èNone |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Consente di specificare il colore da utilizzare per le barre laterali che identificano le righe del documento contenenti informazioni riviste. Il valore predefinito èRed . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Ottiene o imposta la posizione di rendering delle barre di revisione. Il valore predefinito èOutside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Ottiene o imposta la larghezza delle barre di revisione, dei punti. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Consente di specificare se le revisioni vengono renderizzate nei fumetti. Il valore predefinito èNone . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Consente di specificare se il testo originale deve essere visualizzato invece di quello rivisto. Il valore predefinito è`falso` . |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Consente di specificare se le barre di revisione devono essere visualizzate vicino alle linee contenenti contenuto rivisto. Il valore predefinito è`VERO` . |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Consente di specificare se il testo della revisione deve essere contrassegnato con un markup di formattazione speciale. Il valore predefinito è`VERO` . |

## Esempi

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
