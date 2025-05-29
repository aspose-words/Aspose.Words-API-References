---
title: EditableRange.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words per .NET
description: Scopri la proprietà EditableRange Id, accedi e gestisci facilmente gli identificatori degli intervalli modificabili per un maggiore controllo e una maggiore efficienza dei documenti.
type: docs
weight: 40
url: /it/net/aspose.words/editablerange/id/
---
## EditableRange.Id property

Ottiene l'identificatore dell'intervallo modificabile.

```csharp
public int Id { get; }
```

## Osservazioni

La regione deve essere delimitata utilizzando il[`EditableRangeStart`](../editablerangestart/) E[`EditableRangeEnd`](../editablerangeend/)

Gli identificatori di intervallo modificabili dovrebbero essere univoci in tutto il documento e Aspose.Words mantiene automaticamente gli identificatori di intervallo modificabili durante il caricamento, il salvataggio e la combinazione di documenti.

## Esempi

Mostra come lavorare con un intervallo modificabile.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Gli intervalli modificabili consentono di lasciare aperte parti di documenti protetti per la modifica.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// Un intervallo modificabile ben formato ha un nodo iniziale e un nodo finale.
// Questi nodi hanno ID corrispondenti e comprendono nodi modificabili.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Le diverse parti dell'intervallo modificabile sono collegate tra loro.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Possiamo accedere ai tipi di nodo di ogni parte in questo modo. L'intervallo modificabile in sé non è un nodo,
// ma un'entità che consiste in un inizio, una fine e i relativi contenuti racchiusi.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Rimuovi un intervallo modificabile. Tutti i nodi che si trovavano all'interno dell'intervallo rimarranno intatti.
editableRange.Remove();
```

### Guarda anche

* class [EditableRange](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
