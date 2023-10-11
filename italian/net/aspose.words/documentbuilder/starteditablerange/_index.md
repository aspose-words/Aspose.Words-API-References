---
title: DocumentBuilder.StartEditableRange
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Contrassegna la posizione corrente nel documento come inizio di un intervallo modificabile.
type: docs
weight: 640
url: /it/net/aspose.words/documentbuilder/starteditablerange/
---
## DocumentBuilder.StartEditableRange method

Contrassegna la posizione corrente nel documento come inizio di un intervallo modificabile.

```csharp
public EditableRangeStart StartEditableRange()
```

### Valore di ritorno

Il nodo iniziale dell'intervallo modificabile appena creato.

### Osservazioni

L'intervallo modificabile in un documento può sovrapporsi e estendersi a qualsiasi intervallo. Per creare un intervallo modificabile valido devi chiamarli entrambi`StartEditableRange` E[`EndEditableRange`](../endeditablerange/) o[`EndEditableRange`](../endeditablerange/) metodi.

L'intervallo modificabile formato in modo errato verrà ignorato quando il documento viene salvato.

### Esempi

Mostra come creare intervalli modificabili nidificati.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// Crea due intervalli modificabili nidificati.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// Attualmente, il cursore di inserimento del nodo del generatore di documenti si trova in più di un intervallo modificabile in corso.
// Quando vogliamo terminare un intervallo modificabile in questa situazione,
// dobbiamo specificare quale degli intervalli desideriamo terminare passando il relativo nodo EditableRangeStart.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Se un'area di testo ha due intervalli modificabili sovrapposti con gruppi specificati,
// al gruppo combinato di utenti esclusi da entrambi i gruppi non è consentito modificarlo.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

Mostra come lavorare con un intervallo modificabile.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Gli intervalli modificabili ci consentono di lasciare parti di documenti protetti aperte per la modifica.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// Un intervallo modificabile ben formato ha un nodo iniziale e un nodo finale.
// Questi nodi hanno ID corrispondenti e comprendono nodi modificabili.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Parti diverse dell'intervallo modificabile si collegano tra loro.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Possiamo accedere ai tipi di nodo di ciascuna parte in questo modo. L'intervallo modificabile in sé non è un nodo,
// ma un'entità che consiste in un inizio, una fine e il contenuto racchiuso.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Rimuove un intervallo modificabile. Tutti i nodi che erano all'interno dell'intervallo rimarranno intatti.
editableRange.Remove();
```

### Guarda anche

* class [EditableRangeStart](../../editablerangestart/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


