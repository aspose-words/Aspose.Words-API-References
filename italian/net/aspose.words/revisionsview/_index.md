---
title: RevisionsView Enum
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words per .NET
description: Aspose.Words.RevisionsView enum. Permette di specificare se lavorare con la versione originale o rivista di un documento in C#.
type: docs
weight: 4810
url: /it/net/aspose.words/revisionsview/
---
## RevisionsView enumeration

Permette di specificare se lavorare con la versione originale o rivista di un documento.

```csharp
public enum RevisionsView
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Original | `0` | Specifica la versione originale di un documento. |
| Final | `1` | Specifica la versione rivista di un documento. |

## Esempi

Mostra come passare dalla visualizzazione modificata a quella originale di un documento.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Visualizza l'oggetto documento come se tutte le revisioni fossero accettate. Attualmente supporta le etichette degli elenchi.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
