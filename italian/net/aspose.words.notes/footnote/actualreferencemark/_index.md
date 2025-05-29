---
title: Footnote.ActualReferenceMark
linktitle: ActualReferenceMark
articleTitle: ActualReferenceMark
second_title: Aspose.Words per .NET
description: Scopri la proprietà Footnote ActualReferenceMark per accedere al testo preciso dei segni di riferimento nei tuoi documenti, migliorando chiarezza e organizzazione.
type: docs
weight: 20
url: /it/net/aspose.words.notes/footnote/actualreferencemark/
---
## Footnote.ActualReferenceMark property

Ottiene il testo effettivo del segno di riferimento visualizzato nel documento per questa nota a piè di pagina.

```csharp
public string ActualReferenceMark { get; }
```

## Osservazioni

Per popolare inizialmente i valori di questa proprietà per tutti i segni di riferimento del documento, o per aggiornare i valori dopo le modifiche nel documento che potrebbero influenzare i segni di riferimento, è necessario eseguire [`UpdateActualReferenceMarks`](../../../aspose.words/document/updateactualreferencemarks/) metodo. Aggiornamento dei campi ([`UpdateFields`](../../../aspose.words/document/updatefields/) ) potrebbe anche essere necessario per ottenere il risultato corretto.

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

* class [Footnote](../)
* spazio dei nomi [Aspose.Words.Notes](../../../aspose.words.notes/)
* assemblea [Aspose.Words](../../../)
