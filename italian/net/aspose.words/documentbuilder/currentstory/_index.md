---
title: DocumentBuilder.CurrentStory
linktitle: CurrentStory
articleTitle: CurrentStory
second_title: Aspose.Words per .NET
description: Scopri la proprietà CurrentStory di DocumentBuilder per accedere e gestire in modo efficiente la storia selezionata, migliorando così l'esperienza di modifica dei documenti.
type: docs
weight: 70
url: /it/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

Ottiene la storia attualmente selezionata in questo[`DocumentBuilder`](../) .

```csharp
public Story CurrentStory { get; }
```

## Esempi

Mostra come lavorare con la storia corrente di un generatore di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Una storia è un tipo di nodo che ha nodi Paragrafo figlio, come un corpo.
Assert.AreEqual(builder.CurrentStory, doc.FirstSection.Body);
Assert.AreEqual(builder.CurrentStory, builder.CurrentParagraph.ParentNode);
Assert.AreEqual(StoryType.MainText, builder.CurrentStory.StoryType);

builder.CurrentStory.AppendParagraph("Text added to current Story.");

// Una storia può contenere anche tabelle.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndTable();

Assert.IsTrue(builder.CurrentStory.Tables.Contains(table));
```

### Guarda anche

* class [Story](../../story/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
