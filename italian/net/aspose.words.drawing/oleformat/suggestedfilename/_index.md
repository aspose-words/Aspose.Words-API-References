---
title: OleFormat.SuggestedFileName
linktitle: SuggestedFileName
articleTitle: SuggestedFileName
second_title: Aspose.Words per .NET
description: Scopri la proprietà SuggestedFileName di OleFormat per recuperare facilmente il nome file consigliato per salvare senza problemi gli oggetti incorporati.
type: docs
weight: 130
url: /it/net/aspose.words.drawing/oleformat/suggestedfilename/
---
## OleFormat.SuggestedFileName property

Ottiene il nome file suggerito per l'oggetto incorporato corrente se si desidera salvarlo in un file.

```csharp
public string SuggestedFileName { get; }
```

## Esempi

Mostra come ottenere il nome file suggerito per un oggetto OLE.

```csharp
Document doc = new Document(MyDir + "OLE shape.rtf");

Shape oleShape = (Shape)doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true);

// Gli oggetti OLE possono fornire un nome file e un'estensione suggeriti,
// che possiamo utilizzare quando salviamo il contenuto dell'oggetto in un file nel file system locale.
string suggestedFileName = oleShape.OleFormat.SuggestedFileName;

Assert.AreEqual("CSV.csv", suggestedFileName);

using (FileStream fileStream = new FileStream(ArtifactsDir + suggestedFileName, FileMode.Create))
{
    oleShape.OleFormat.Save(fileStream);
}
```

### Guarda anche

* class [OleFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
