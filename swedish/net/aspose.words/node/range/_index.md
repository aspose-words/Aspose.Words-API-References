---
title: Node.Range
linktitle: Range
articleTitle: Range
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Node Range och få enkelt tillgång till ett Range-objekt som definierar dokumentsegmentet i din nod för förbättrad innehållshantering.
type: docs
weight: 80
url: /sv/net/aspose.words/node/range/
---
## Node.Range property

Returnerar en[`Range`](../../range/)objekt som representerar den del av ett dokument som finns i denna nod.

```csharp
public Range Range { get; }
```

## Exempel

Visar hur man tar bort alla noder från ett intervall.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till text i det första avsnittet i dokumentet och lägg sedan till ett annat avsnitt.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// Ta bort den första sektionen helt genom att ta bort alla noder
// inom sitt intervall, inklusive själva sektionen.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### Se även

* class [Range](../../range/)
* class [Node](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
