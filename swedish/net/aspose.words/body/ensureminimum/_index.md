---
title: Body.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words för .NET
description: Optimera ditt innehåll med metoden Body EnsureMinimum. Lägg automatiskt till ett tomt stycke om det sista underordnade stycket inte är ett stycke för bättre formatering.
type: docs
weight: 70
url: /sv/net/aspose.words/body/ensureminimum/
---
## Body.EnsureMinimum method

Om det sista underordnade stycket inte är ett stycke skapas och läggs till ett tomt stycke.

```csharp
public void EnsureMinimum()
```

## Exempel

Tar bort huvudtexten från alla avsnitt i dokumentet, men lämnar själva avsnitten kvar.

```csharp
Document doc = new Document();

// Ett tomt dokument innehåller ett avsnitt, en brödtext och ett stycke.
// Anropa metoden "RemoveAllChildren" för att ta bort alla dessa noder,
// och slutar med en dokumentnod utan barn.
doc.RemoveAllChildren();

// Det här dokumentet har nu inga sammansatta undernoder som vi kan lägga till innehåll till.
// Om vi vill redigera den måste vi fylla i dess nodsamling igen.
// Skapa först en ny sektion och lägg sedan till den som ett underordnat avsnitt till rotdokumentnoden.
Section section = new Section(doc);
doc.AppendChild(section);

// En sektion behöver en brödtext, som innehåller och visar allt dess innehåll
// på sidan mellan avsnittets sidhuvud och sidfot.
Body body = new Body(doc);
section.AppendChild(body);

// Den här kroppen har inga underordnade element, så vi kan inte lägga till körningar i den ännu.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

 // Anropa "EnsureMinimum" för att se till att den här texten innehåller minst ett tomt stycke.
body.EnsureMinimum();

// Nu kan vi lägga till körningar i brödtexten och få dokumentet att visa dem.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Se även

* class [Body](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
