---
title: RevisionOptions.InsertCellColor
linktitle: InsertCellColor
articleTitle: InsertCellColor
second_title: Aspose.Words per .NET
description: Personalizza il tuo foglio di calcolo con la proprietà InsertCellColor in RevisionOptions. Scegli il colore che preferisci per le celle inserite: il colore predefinito è il blu!
type: docs
weight: 50
url: /it/net/aspose.words.layout/revisionoptions/insertcellcolor/
---
## RevisionOptions.InsertCellColor property

Permette di specificare il colore da utilizzare per le celle inseriteInsertion . Il valore predefinito èBlue .

```csharp
public RevisionColor InsertCellColor { get; set; }
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
