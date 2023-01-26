---
title: EndEditableRange
second_title: Aspose.Words per .NET API Reference
description: Contrassegna la posizione corrente nel documento come fine di un intervallo modificabile.
type: docs
weight: 210
url: /it/net/aspose.words/documentbuilder/endeditablerange/
---
## EndEditableRange() {#endeditablerange}

Contrassegna la posizione corrente nel documento come fine di un intervallo modificabile.

```csharp
public EditableRangeEnd EndEditableRange()
```

### Valore di ritorno

Il nodo finale dell'intervallo modificabile appena creato.

### Osservazioni

L'intervallo modificabile in un documento può sovrapporsi e estendersi a qualsiasi intervallo. Per creare un intervallo modificabile valido devi chiamare entrambi[`StartEditableRange`](../starteditablerange/) e`EndEditableRange` o`EndEditableRange`metodi.

L'intervallo modificabile formato in modo errato verrà ignorato quando il documento viene salvato.

### Esempi

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

// Diverse parti dell'intervallo modificabile si collegano tra loro.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Possiamo accedere ai tipi di nodo di ciascuna parte in questo modo. L'intervallo modificabile stesso non è un nodo,
// ma un'entità che consiste in un inizio, una fine e il loro contenuto racchiuso.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Rimuove un intervallo modificabile. Tutti i nodi che erano all'interno dell'intervallo rimarranno intatti.
editableRange.Remove();
```

### Guarda anche

* class [EditableRangeEnd](../../editablerangeend/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)

---

## EndEditableRange(EditableRangeStart) {#endeditablerange_1}

Contrassegna la posizione corrente nel documento come fine di un intervallo modificabile.

```csharp
public EditableRangeEnd EndEditableRange(EditableRangeStart start)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| start | EditableRangeStart | Questo intervallo modificabile inizia. |

### Valore di ritorno

Il nodo finale dell'intervallo modificabile appena creato.

### Osservazioni

Utilizzare questo sovraccarico durante la creazione di intervalli modificabili nidificati.

L'intervallo modificabile in un documento può sovrapporsi e estendersi a qualsiasi intervallo. Per creare un intervallo modificabile valido devi chiamare entrambi[`StartEditableRange`](../starteditablerange/) e`EndEditableRange` o`EndEditableRange`metodi.

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
// dobbiamo specificare quale degli intervalli vogliamo terminare passando il suo nodo EditableRangeStart.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Se un'area di testo ha due intervalli modificabili sovrapposti con gruppi specificati,
// al gruppo combinato di utenti esclusi da entrambi i gruppi viene impedito di modificarlo.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

### Guarda anche

* class [EditableRangeEnd](../../editablerangeend/)
* class [EditableRangeStart](../../editablerangestart/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
