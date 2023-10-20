---
title: RevisionOptions.ShowInBalloons
linktitle: ShowInBalloons
articleTitle: ShowInBalloons
second_title: Aspose.Words per .NET
description: RevisionOptions ShowInBalloons proprietà. Permette di specificare se le revisioni vengono renderizzate nei fumetti. Il valore predefinito èNone  in C#.
type: docs
weight: 160
url: /it/net/aspose.words.layout/revisionoptions/showinballoons/
---
## RevisionOptions.ShowInBalloons property

Permette di specificare se le revisioni vengono renderizzate nei fumetti. Il valore predefinito èNone .

```csharp
public ShowInBalloons ShowInBalloons { get; set; }
```

## Osservazioni

Tieni presente che le revisioni non vengono visualizzate nei fumetti perShowInAnnotations .

## Esempi

Mostra come visualizzare le revisioni nei fumetti.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Per impostazione predefinita, il testo che è una revisione ha un colore diverso per differenziarlo dall'altro testo non di revisione.
// Imposta un'opzione di revisione per mostrare maggiori dettagli su ciascuna revisione in un fumetto sul margine destro della pagina.
doc.LayoutOptions.RevisionOptions.ShowInBalloons = ShowInBalloons.FormatAndDelete;
doc.Save(ArtifactsDir + "Revision.ShowRevisionBalloons.pdf");
```

Mostra come modificare l'aspetto delle revisioni.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Ottiene l'oggetto RevisionOptions che controlla l'aspetto delle revisioni.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Visualizza le revisioni dell'inserimento in verde e corsivo.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Visualizza le revisioni di eliminazione in rosso e in grassetto.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Lo stesso testo apparirà due volte in una revisione del movimento:
// una volta al punto di partenza e una volta alla destinazione di arrivo.
// Rende il testo della revisione spostata in giallo con un doppio barrato
// e doppia sottolineatura in blu nella revisione spostata.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Rende le revisioni del formato in rosso scuro e grassetto.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Posiziona una spessa barra blu scuro sul lato sinistro della pagina accanto alle righe interessate dalle revisioni.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Mostra i segni di revisione e il testo originale.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Ottieni movimento, eliminazione, revisioni di formattazione e commenti da visualizzare in fumetti verdi
// sul lato destro della pagina.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Queste funzionalità sono applicabili solo a formati come .pdf o .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Guarda anche

* enum [ShowInBalloons](../../showinballoons/)
* class [RevisionOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
