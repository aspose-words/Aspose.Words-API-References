---
title: RevisionColor Enum
linktitle: RevisionColor
articleTitle: RevisionColor
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Layout.RevisionColor per personalizzare i colori di revisione dei documenti, migliorando la chiarezza e la collaborazione nei tuoi documenti.
type: docs
weight: 3830
url: /it/net/aspose.words.layout/revisioncolor/
---
## RevisionColor enumeration

Consente di specificare il colore delle revisioni del documento.

```csharp
public enum RevisionColor
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | `0` | Predefinito. |
| Black | `1` | Rappresenta 000000 colore. |
| Blue | `2` | Rappresenta il colore 2e97d3. |
| BrightGreen | `3` | Rappresenta il colore 84a35b. |
| ClassicBlue | `4` | Rappresenta il colore 0000ff. |
| ClassicRed | `5` | Rappresenta il colore ff0000. |
| DarkBlue | `6` | Rappresenta 376e96 colori. |
| DarkRed | `7` | Rappresenta 881824 colori. |
| DarkYellow | `8` | Rappresenta il colore e09a2b. |
| Gray25 | `9` | Rappresenta il colore a0a3a9. |
| Gray50 | `10` | Rappresenta 50565 colori. |
| Green | `11` | Rappresenta 2c6234 colori. |
| Pink | `12` | Rappresenta il colore ce338f. |
| Red | `13` | Rappresenta il colore b5082e. |
| Teal | `14` | Rappresenta il colore 1b9cab. |
| Turquoise | `15` | Rappresenta il colore 3eafc2. |
| Violet | `16` | Rappresenta 633277 colori. |
| White | `17` | Rappresenta il colore ffffff. |
| Yellow | `18` | Rappresenta il colore fad272. |
| LightPink | `19` | Rappresenta il colore fce6f4. |
| LightBlue | `20` | Rappresenta il colore e1f2fa. |
| LightYellow | `21` | Rappresenta il colore fef4de. |
| LightPurple | `22` | Rappresenta il colore del mento. |
| LightOrange | `23` | Rappresenta il colore fce3d0. |
| LightGreen | `24` | Rappresenta il colore e9f8ce. |
| Gray | `25` | Rappresenta il colore efeded. |
| NoHighlight | `26` | Non viene utilizzato alcun colore per evidenziare le modifiche alla revisione. |
| ByAuthor | `27` | Le revisioni di ciascun autore ricevono il proprio colore per l'evidenziazione da un set predefinito di colori ad alto contrasto. |

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
