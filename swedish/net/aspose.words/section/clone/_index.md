---
title: Section.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words för .NET
description: Duplicera enkelt avsnitt med vår metod för sektionskloning. Effektivisera ditt arbetsflöde och öka produktiviteten med detta kraftfulla verktyg!
type: docs
weight: 130
url: /sv/net/aspose.words/section/clone/
---
## Section.Clone method

Skapar en kopia av detta avsnitt.

```csharp
public Section Clone()
```

## Exempel

Visar hur man lägger till och tar bort avsnitt i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Ta bort det första avsnittet från dokumentet.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Lägg till en kopia av det som nu är det första avsnittet i slutet av dokumentet.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Se även

* class [Section](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
