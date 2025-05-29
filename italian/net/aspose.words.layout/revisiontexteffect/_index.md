---
title: RevisionTextEffect Enum
linktitle: RevisionTextEffect
articleTitle: RevisionTextEffect
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Layout.RevisionTextEffect per migliorare le revisioni dei documenti con effetti di decorazione del testo unici. Migliora la tua esperienza di editing!
type: docs
weight: 3850
url: /it/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

Consente di specificare l'effetto decorativo per le revisioni del testo del documento.

```csharp
public enum RevisionTextEffect
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Al contenuto rivisto non sono stati applicati effetti speciali. Ciò corrisponde aNoHighlight . |
| Color | `1` | Il contenuto rivisto è evidenziato solo con il colore. |
| Bold | `2` | Il contenuto rivisto è in grassetto e colorato. |
| Italic | `3` | Il contenuto rivisto è in corsivo e colorato. |
| Underline | `4` | Il contenuto rivisto è sottolineato e colorato. |
| DoubleUnderline | `5` | Il contenuto rivisto è sottolineato due volte e colorato. |
| StrikeThrough | `6` | Il contenuto rivisto è stato barrato e colorato. |
| DoubleStrikeThrough | `7` | Il contenuto rivisto è stato doppiamente tratteggiato e colorato. |
| Hidden | `8` | Il contenuto rivisto è nascosto. |

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

* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout/)
* assemblea [Aspose.Words](../../)
