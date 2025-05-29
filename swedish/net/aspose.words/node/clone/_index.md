---
title: Node.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words för .NET
description: Duplicera enkelt noder med Node Clone-metoden. Förbättra din utvecklingsprocess och effektivisera projektets effektivitet idag!
type: docs
weight: 100
url: /sv/net/aspose.words/node/clone/
---
## Node.Clone method

Skapar en duplikat av noden.

```csharp
public Node Clone(bool isCloneChildren)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| isCloneChildren | Boolean | Sant för att rekursivt klona underträdet under den angivna noden; falskt för att endast klona själva noden. |

### Returvärde

Den klonade noden.

## Anmärkningar

Den här metoden fungerar som en kopieringskonstruktor för noder. Den klonade noden har ingen förälder, men tillhör samma dokument som den ursprungliga noden.

Den här metoden utför alltid en djup kopia av noden.*isCloneChildren* parameter anger om alla undernoder också ska kopieras.

## Exempel

Visar hur man klonar en sammansatt nod.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Nedan följer två sätt att klona en sammansatt nod.
// 1 - Skapa en klon av en nod och skapa även en klon av var och en av dess undernoder.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - Skapa en klon av en nod helt för sig själv utan några underordnade noder.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

### Se även

* class [Node](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
