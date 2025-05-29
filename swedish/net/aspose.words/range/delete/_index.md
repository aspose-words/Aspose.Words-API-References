---
title: Range.Delete
linktitle: Delete
articleTitle: Delete
second_title: Aspose.Words för .NET
description: Ta effektivt bort alla tecken inom ett angivet intervall med hjälp av metoden Områdesradering. Förenkla dina textredigeringsuppgifter utan ansträngning!
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

* class [Range](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
