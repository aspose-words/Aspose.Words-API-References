---
title: ShowInBalloons Enum
linktitle: ShowInBalloons
articleTitle: ShowInBalloons
second_title: Aspose.Words per .NET
description: Scopri come l'enum Aspose.Words.Layout.ShowInBalloons migliora la modifica dei documenti controllando le revisioni visibili nei fumetti per una collaborazione più chiara.
type: docs
weight: 3860
url: /it/net/aspose.words.layout/showinballoons/
---
## ShowInBalloons enumeration

Specifica quali revisioni vengono visualizzate nei fumetti.

```csharp
public enum ShowInBalloons
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Esegue l'inserimento, l'eliminazione e la formattazione delle revisioni in linea. |
| Format | `1` | Esegue l'inserimento e l'eliminazione delle revisioni in linea, formatta le revisioni nei fumetti. |
| FormatAndDelete | `2` | Esegue l'inserimento delle revisioni in linea, elimina e formatta le revisioni nei fumetti. |

## Osservazioni

Nota che le revisioni non vengono visualizzate nei fumetti perShowInAnnotations .

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
