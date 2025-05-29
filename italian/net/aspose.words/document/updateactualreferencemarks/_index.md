---
title: Document.UpdateActualReferenceMarks
linktitle: UpdateActualReferenceMarks
articleTitle: UpdateActualReferenceMarks
second_title: Aspose.Words per .NET
description: Aggiorna senza sforzo tutte le note a piè di pagina e le note di chiusura nel tuo documento con il metodo Document UpdateActualReferenceMarks, migliorando precisione ed efficienza.
type: docs
weight: 800
url: /it/net/aspose.words/document/updateactualreferencemarks/
---
## Document.UpdateActualReferenceMarks method

Aggiorna il[`ActualReferenceMark`](../../../aspose.words.notes/footnote/actualreferencemark/) proprietà di tutte le note a piè di pagina e di chiusura nel documento.

```csharp
public void UpdateActualReferenceMarks()
```

## Osservazioni

Aggiornamento dei campi ([`UpdateFields`](../updatefields/) ) potrebbe essere necessario per ottenere il risultato corretto.

## Esempi

Mostra come ottenere l'effettivo segno di riferimento della nota a piè di pagina.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

Footnote footnote = (Footnote)doc.GetChild(NodeType.Footnote, 1, true);
doc.UpdateFields();
doc.UpdateActualReferenceMarks();

Assert.AreEqual("1", footnote.ActualReferenceMark);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
