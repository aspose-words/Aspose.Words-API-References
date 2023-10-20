---
title: RevisionOptions.MovedFromTextEffect
linktitle: MovedFromTextEffect
articleTitle: MovedFromTextEffect
second_title: Aspose.Words per .NET
description: RevisionOptions MovedFromTextEffect proprietà. Permette di specificare leffetto da applicare alle aree da cui è stato spostato il contenutoMoving . Il valore predefinito èDoubleStrikeThrough in C#.
type: docs
weight: 80
url: /it/net/aspose.words.layout/revisionoptions/movedfromtexteffect/
---
## RevisionOptions.MovedFromTextEffect property

Permette di specificare l'effetto da applicare alle aree da cui è stato spostato il contenutoMoving . Il valore predefinito èDoubleStrikeThrough

```csharp
public RevisionTextEffect MovedFromTextEffect { get; set; }
```

## Esempi

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

* enum [RevisionTextEffect](../../revisiontexteffect/)
* class [RevisionOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
