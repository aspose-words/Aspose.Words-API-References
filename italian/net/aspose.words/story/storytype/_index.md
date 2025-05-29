---
title: Story.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words per .NET
description: Scopri la proprietà StoryType per identificare e categorizzare facilmente le tue storie, migliorandone l'organizzazione e ottimizzando la tua esperienza narrativa.
type: docs
weight: 40
url: /it/net/aspose.words/story/storytype/
---
## Story.StoryType property

Ottiene il tipo di questa storia.

```csharp
public StoryType StoryType { get; }
```

## Esempi

Mostra come rimuovere tutte le forme da un nodo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilizza un DocumentBuilder per inserire una forma. Questa è una forma in linea,
// che ha un Paragrafo padre, che è un nodo figlio del Corpo della prima sezione.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Possiamo eliminare tutte le forme dai paragrafi figlio di questo Corpo.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Guarda anche

* enum [StoryType](../../storytype/)
* class [Story](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
