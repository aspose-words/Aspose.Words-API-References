---
title: Range.Delete
linktitle: Delete
articleTitle: Delete
second_title: Aspose.Words för .NET
description: Range Delete metod. Tar bort alla tecken i intervallet i C#.
type: docs
weight: 70
url: /sv/net/aspose.words/range/delete/
---
## Range.Delete method

Tar bort alla tecken i intervallet.

```csharp
public void Delete()
```

## Exempel

Visar hur man tar bort alla noder från ett område.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till text i det första avsnittet i dokumentet och lägg sedan till ytterligare ett avsnitt.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// Ta bort det första avsnittet helt genom att ta bort alla noder
// inom sitt intervall, inklusive själva avsnittet.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### Se även

* class [Range](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
