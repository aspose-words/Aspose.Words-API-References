---
title: DocumentBuilder.EndEditableRange
linktitle: EndEditableRange
articleTitle: EndEditableRange
second_title: Aspose.Words per .NET
description: Scopri il metodo EndEditableRange di DocumentBuilder per contrassegnare in modo efficiente le sezioni modificabili nei tuoi documenti, migliorando il flusso di lavoro di modifica.
type: docs
weight: 230
url: /it/net/aspose.words/documentbuilder/endeditablerange/
---
## EndEditableRange() {#endeditablerange}

Contrassegna la posizione corrente nel documento come fine di un intervallo modificabile.

```csharp
public EditableRangeEnd EndEditableRange()
```

### Valore di ritorno

Il nodo finale dell'intervallo modificabile appena creato.

## Osservazioni

Gli intervalli modificabili in un documento possono sovrapporsi e estendersi su qualsiasi intervallo. Per creare un intervallo modificabile valido, è necessario chiamare entrambi i metodi [`StartEditableRange`](../starteditablerange/) E`EndEditableRange` o`EndEditableRange` metodi.

Gli intervalli modificabili mal formattati verranno ignorati al momento del salvataggio del documento.

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

* class [EditableRangeEnd](../../editablerangeend/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## EndEditableRange(*[EditableRangeStart](../../editablerangestart/)*) {#endeditablerange_1}

Contrassegna la posizione corrente nel documento come fine di un intervallo modificabile.

```csharp
public EditableRangeEnd EndEditableRange(EditableRangeStart start)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| start | EditableRangeStart | Inizio di questo intervallo modificabile. |

### Valore di ritorno

Il nodo finale dell'intervallo modificabile appena creato.

## Osservazioni

Utilizzare questo sovraccarico durante la creazione di intervalli modificabili annidati.

Gli intervalli modificabili in un documento possono sovrapporsi e estendersi su qualsiasi intervallo. Per creare un intervallo modificabile valido, è necessario chiamare entrambi i metodi [`StartEditableRange`](../starteditablerange/) E`EndEditableRange` o`EndEditableRange` metodi.

Gli intervalli modificabili mal formattati verranno ignorati al momento del salvataggio del documento.

## Esempi

Mostra come creare intervalli modificabili nidificati.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// Crea due intervalli modificabili annidati.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// Attualmente, il cursore di inserimento del nodo del generatore di documenti si trova in più di un intervallo modificabile in corso.
// Quando vogliamo terminare un intervallo modificabile in questa situazione,
// dobbiamo specificare quale intervallo vogliamo che termini passando il relativo nodo EditableRangeStart.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Se una regione di testo ha due intervalli modificabili sovrapposti con gruppi specificati,
// al gruppo combinato di utenti esclusi da entrambi i gruppi è impedito di modificarlo.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

### Guarda anche

* class [EditableRangeEnd](../../editablerangeend/)
* class [EditableRangeStart](../../editablerangestart/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
