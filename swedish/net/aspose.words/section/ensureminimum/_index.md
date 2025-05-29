---
title: Section.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words för .NET
description: Optimera ditt innehåll med EnsureMinimum-metoden, vilket garanterar att varje avsnitt innehåller en brödtext med ett stycke för ökad tydlighet och struktur.
type: docs
weight: 150
url: /sv/net/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method

Säkerställer att sektionen har[`Body`](../body/) med en[`Paragraph`](../../paragraph/) .

```csharp
public void EnsureMinimum()
```

## Exempel

Visar hur man förbereder en ny sektionsnod för redigering.

```csharp
Document doc = new Document();

// Ett tomt dokument kommer med ett avsnitt, som har en brödtext, som i sin tur har ett stycke.
// Vi kan lägga till innehåll i det här dokumentet genom att lägga till element som textsekvenser, former eller tabeller i stycket.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Om vi lägger till en ny sektion som denna, kommer den inte att ha någon brödtext eller några andra underordnade noder.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Kör metoden "EnsureMinimum" för att lägga till en brödtext och ett stycke i det här avsnittet för att börja redigera det.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Se även

* class [Section](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
