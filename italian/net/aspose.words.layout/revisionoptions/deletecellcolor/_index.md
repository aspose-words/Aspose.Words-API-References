---
title: RevisionOptions.DeleteCellColor
linktitle: DeleteCellColor
articleTitle: DeleteCellColor
second_title: Aspose.Words per .NET
description: Personalizza il tuo foglio di calcolo con la proprietà DeleteCellColor di RevisionOptions. Imposta facilmente un colore univoco per le celle eliminate, migliorando la chiarezza e l'organizzazione.
type: docs
weight: 20
url: /it/net/aspose.words.layout/revisionoptions/deletecellcolor/
---
## RevisionOptions.DeleteCellColor property

Consente di specificare il colore da utilizzare per le celle eliminateDeletion . Il valore predefinito èPink .

```csharp
public RevisionColor DeleteCellColor { get; set; }
```

## Esempi

Mostra come lavorare con il colore di revisione delle celle di inserimento/eliminazione.

```csharp
Document doc = new Document(MyDir + "Cell revisions.docx");

doc.LayoutOptions.RevisionOptions.InsertCellColor = RevisionColor.LightBlue;
doc.LayoutOptions.RevisionOptions.DeleteCellColor = RevisionColor.DarkRed;

doc.Save(ArtifactsDir + "Revision.RevisionCellColor.pdf");
```

### Guarda anche

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
