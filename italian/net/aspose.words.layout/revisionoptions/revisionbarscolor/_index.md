---
title: RevisionOptions.RevisionBarsColor
linktitle: RevisionBarsColor
articleTitle: RevisionBarsColor
second_title: Aspose.Words per .NET
description: Personalizza il colore delle barre di revisione del tuo documento per evidenziare facilmente le righe revisionate. Il colore predefinito è il rosso, ma scegli qualsiasi colore per una visualizzazione più chiara!
type: docs
weight: 150
url: /it/net/aspose.words.layout/revisionoptions/revisionbarscolor/
---
## RevisionOptions.RevisionBarsColor property

Consente di specificare il colore da utilizzare per le barre laterali che identificano le righe del documento contenenti informazioni riviste. Il valore predefinito èRed .

```csharp
public RevisionColor RevisionBarsColor { get; set; }
```

## Osservazioni

Impostando questa proprietà suByAuthor ONoHighlight values nasconderà le barre di revisione dal layout.

## Esempi

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

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
