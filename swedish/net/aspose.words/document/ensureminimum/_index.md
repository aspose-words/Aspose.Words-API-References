---
title: Document.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words för .NET
description: Lär dig hur du använder EnsureMinimum-metoden för att automatiskt skapa ett avsnitt och stycke i dokument, vilket säkerställer fullständigt och organiserat innehåll.
type: docs
weight: 620
url: /sv/net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

Om dokumentet inte innehåller några avsnitt skapas ett avsnitt med ett stycke.

```csharp
public void EnsureMinimum()
```

## Exempel

Visar hur man säkerställer att ett dokument innehåller den minimala uppsättning noder som krävs för att redigera dess innehåll.

```csharp
// Ett nyskapat dokument innehåller ett underavsnitt, som inkluderar ett underordnat brödtext och ett underordnat stycke.
// Vi kan redigera dokumentets innehåll genom att lägga till noder som Runs eller inline Shapes i stycket.
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// Detta är den minsta uppsättning noder som vi behöver för att kunna redigera dokumentet.
// Vi kommer inte längre att kunna redigera dokumentet om vi tar bort någon av dem.
doc.RemoveAllChildren();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);

// Anropa den här metoden för att se till att dokumentet har minst dessa tre noder så att vi kan redigera det igen.
doc.EnsureMinimum();

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);

((Paragraph)nodes[2]).Runs.Add(new Run(doc, "Hello world!"));
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
