---
title: Enum RevisionColor
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Layout.RevisionColor enum. Consente di specificare il colore delle revisioni del documento.
type: docs
weight: 3180
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
| Black | `1` | Rappresenta 000000 colori. |
| Blue | `2` | Rappresenta il colore 2e97d3. |
| BrightGreen | `3` | Rappresenta il colore 84a35b. |
| ClassicBlue | `4` | Rappresenta il colore 0000ff. |
| ClassicRed | `5` | Rappresenta il colore ff0000. |
| DarkBlue | `6` | Rappresenta il colore 376e96. |
| DarkRed | `7` | Rappresenta 881824 colori. |
| DarkYellow | `8` | Rappresenta il colore e09a2b. |
| Gray25 | `9` | Rappresenta un colore a0a3a9. |
| Gray50 | `10` | Rappresenta il colore 50565e. |
| Green | `11` | Rappresenta il colore 2c6234. |
| Pink | `12` | Rappresenta il colore ce338f. |
| Red | `13` | Rappresenta il colore b5082e. |
| Teal | `14` | Rappresenta il colore della cabina 1b9. |
| Turquoise | `15` | Rappresenta il colore 3eafc2. |
| Violet | `16` | Rappresenta 633277 colori. |
| White | `17` | Rappresenta il colore ffffff. |
| Yellow | `18` | Rappresenta il colore fad272. |
| NoHighlight | `19` | Nessun colore viene utilizzato per evidenziare le modifiche alla revisione. |
| ByAuthor | `20` | Le revisioni di ogni autore ricevono il proprio colore per l'evidenziazione da un set predefinito di colori ad alto contrasto. |

### Esempi

Mostra come modificare l'aspetto delle revisioni in un documento di output sottoposto a rendering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una revisione, quindi cambia il colore di tutte le revisioni in verde.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Rimuove la barra che appare a sinistra di ogni riga modificata.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout/)
* assemblea [Aspose.Words](../../)


