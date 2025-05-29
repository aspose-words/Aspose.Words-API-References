---
title: EditableRangeStart.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words per .NET
description: Scopri la proprietà NodeType EditableRangeStart: migliora la modifica dei tuoi documenti con una gestione degli intervalli fluida e un'esperienza utente migliorata!
type: docs
weight: 30
url: /it/net/aspose.words/editablerangestart/nodetype/
---
## EditableRangeStart.NodeType property

RestituisceEditableRangeStart .

```csharp
public override NodeType NodeType { get; }
```

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

* enum [NodeType](../../nodetype/)
* class [EditableRangeStart](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
