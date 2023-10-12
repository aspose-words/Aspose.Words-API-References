---
title: Enum RevisionTextEffect
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Layout.RevisionTextEffect enum. Permette di specificare leffetto decorativo per le revisioni del testo del documento.
type: docs
weight: 3400
url: /it/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

Permette di specificare l'effetto decorativo per le revisioni del testo del documento.

```csharp
public enum RevisionTextEffect
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Al contenuto rivisto non sono applicati effetti speciali. Ciò corrisponde aNoHighlight . |
| Color | `1` | I contenuti revisionati sono evidenziati solo con il colore. |
| Bold | `2` | I contenuti rivisti sono resi in grassetto e colorati. |
| Italic | `3` | Il contenuto rivisto è reso in corsivo e colorato. |
| Underline | `4` | Il contenuto rivisto è sottolineato e colorato. |
| DoubleUnderline | `5` | Il contenuto rivisto è sottolineato due volte e colorato. |
| StrikeThrough | `6` | Il contenuto rivisto viene cancellato e colorato. |
| DoubleStrikeThrough | `7` | Il contenuto rivisto viene doppiato e colorato. |
| Hidden | `8` | Il contenuto rivisto è nascosto. |

### Esempi

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

* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout/)
* assemblea [Aspose.Words](../../)


