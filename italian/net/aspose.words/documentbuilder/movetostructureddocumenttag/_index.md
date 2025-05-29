---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: Aspose.Words per .NET
description: Passa senza sforzo ai tag dei documenti strutturati con il metodo MoveToStructuredDocumentTag di DocumentBuilder, migliorando l'efficienza della modifica dei documenti.
type: docs
weight: 620
url: /it/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(*int, int*) {#movetostructureddocumenttag_1}

Sposta il cursore su un tag di documento strutturato nella sezione corrente.

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | Indice del tag del documento strutturato a cui spostarsi. |
| characterIndex | Int32 | Indice del carattere all'interno del tag del documento strutturato. Un valore negativo consente di specificare una posizione dalla fine del tag del documento strutturato. Utilizzare -1 per spostarsi alla fine del tag del documento strutturato. Se il tag del documento strutturato si trova a livello di blocco e si desidera spostare il cursore alla fine dell'ultimo paragrafo, specificare -2. |

## Osservazioni

La navigazione viene eseguita all'interno della storia corrente della sezione corrente. Vale a dire, se si sposta il cursore sull'intestazione principale della prima sezione, allora*structuredDocumentTagIndex* ha specificato l'indice del tag del documento strutturato all'interno dell'intestazione di quella sezione.

Quando*structuredDocumentTagIndex* è maggiore o uguale a 0, specifica un indice dall'inizio della sezione, dove 0 è il primo tag del documento strutturato. Quando *structuredDocumentTagIndex*è minore di 0, ha specificato un indice dalla fine della sezione con -1 come ultimo tag del documento strutturato.

## Esempi

Mostra come spostare il cursore di DocumentBuilder all'interno di un tag di documento strutturato.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Esistono diversi modi per spostare il cursore:
// 1 - Passa al primo carattere del tag del documento strutturato tramite l'indice.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - Passa al primo carattere del tag del documento strutturato tramite oggetto.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - Spostarsi alla fine del secondo tag del documento strutturato.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);

// Ottieni il tag del documento strutturato attualmente selezionato.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Guarda anche

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## MoveToStructuredDocumentTag(*[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), int*) {#movetostructureddocumenttag}

Sposta il cursore sul tag del documento strutturato.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | Tag del documento strutturato a cui spostarsi. |
| characterIndex | Int32 | Indice del carattere all'interno del tag del documento strutturato. Un valore negativo consente di specificare una posizione dalla fine del tag del documento strutturato. Utilizzare -1 per spostarsi alla fine del tag del documento strutturato. Se il tag del documento strutturato si trova a livello di blocco e si desidera spostare il cursore alla fine dell'ultimo paragrafo, specificare -2. |

## Esempi

Mostra come spostare il cursore di DocumentBuilder all'interno di un tag di documento strutturato.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Esistono diversi modi per spostare il cursore:
// 1 - Passa al primo carattere del tag del documento strutturato tramite l'indice.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - Passa al primo carattere del tag del documento strutturato tramite oggetto.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - Spostarsi alla fine del secondo tag del documento strutturato.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);

// Ottieni il tag del documento strutturato attualmente selezionato.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Guarda anche

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
