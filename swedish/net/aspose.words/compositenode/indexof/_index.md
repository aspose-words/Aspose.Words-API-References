---
title: CompositeNode.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words för .NET
description: Upptäck hur metoden CompositeNode IndexOf effektivt lokaliserar indexet för en specificerad undernod i arrayen, vilket förbättrar din kodningsupplevelse.
type: docs
weight: 140
url: /sv/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

Returnerar indexet för den angivna undernoden i undernodsmatrisen.

```csharp
public int IndexOf(Node child)
```

## Anmärkningar

Returnerar -1 om noden inte hittas i undernoderna.

## Exempel

Visar hur man hämtar indexet för en given undernod från dess förälder.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// Hämta indexet för det sista stycket i brödtexten i det första avsnittet.
Assert.AreEqual(24, body.GetChildNodes(NodeType.Any, false).IndexOf(body.LastParagraph));
```

### Se även

* class [Node](../../node/)
* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
