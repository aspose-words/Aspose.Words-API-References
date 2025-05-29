---
title: RevisionOptions.ShowInBalloons
linktitle: ShowInBalloons
articleTitle: ShowInBalloons
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShowInBalloons di RevisionOptions! Controlla la visibilità delle revisioni nei fumetti per una maggiore chiarezza del documento. L'impostazione predefinita è Nessuno.
type: docs
weight: 180
url: /it/net/aspose.words.layout/revisionoptions/showinballoons/
---
## RevisionOptions.ShowInBalloons property

Consente di specificare se le revisioni vengono renderizzate nei fumetti. Il valore predefinito èNone .

```csharp
public ShowInBalloons ShowInBalloons { get; set; }
```

## Osservazioni

Nota che le revisioni non vengono visualizzate nei fumetti perShowInAnnotations .

## Esempi

Mostra come visualizzare le revisioni nei fumetti.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Per impostazione predefinita, il testo che costituisce una revisione ha un colore diverso per differenziarlo dal resto del testo non di revisione.
// Imposta un'opzione di revisione per mostrare maggiori dettagli su ogni revisione in un fumetto sul margine destro della pagina.
doc.LayoutOptions.RevisionOptions.ShowInBalloons = ShowInBalloons.FormatAndDelete;
doc.Save(ArtifactsDir + "Revision.ShowRevisionBalloons.pdf");
```

Mostra come modificare l'aspetto delle revisioni.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Ottieni l'oggetto RevisionOptions che controlla l'aspetto delle revisioni.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Visualizza le revisioni di inserimento in verde e corsivo.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Visualizza le revisioni di eliminazione in rosso e in grassetto.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Lo stesso testo apparirà due volte in una revisione del movimento:
// una volta al punto di partenza e una volta alla destinazione di arrivo.
// Rendi il testo della revisione spostata in giallo con una doppia barratura
// e doppia sottolineatura blu nella revisione spostata.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedToTextEffect = RevisionTextEffect.DoubleUnderline;

// Visualizza le revisioni del formato in rosso scuro e in grassetto.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Inserire una barra spessa blu scuro sul lato sinistro della pagina, accanto alle righe interessate dalle revisioni.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Mostra i segni di revisione e il testo originale.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Ottieni che i movimenti, le eliminazioni, le revisioni di formattazione e i commenti vengano visualizzati in palloncini verdi
// sul lato destro della pagina.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Queste funzionalità sono applicabili solo ai formati quali .pdf o .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Guarda anche

* enum [ShowInBalloons](../../showinballoons/)
* class [RevisionOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
