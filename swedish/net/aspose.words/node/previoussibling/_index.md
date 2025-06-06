---
title: Node.PreviousSibling
linktitle: PreviousSibling
articleTitle: PreviousSibling
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Node PreviousSibling för att enkelt komma åt noden som kommer före din nuvarande nod, vilket förbättrar dina DOM-manipulationsfärdigheter.
type: docs
weight: 70
url: /sv/net/aspose.words/node/previoussibling/
---
## Node.PreviousSibling property

Hämtar noden som omedelbart föregår denna nod.

```csharp
public Node PreviousSibling { get; }
```

## Anmärkningar

Om det inte finns någon föregående nod, en`null` returneras.

## Exempel

Visar hur man använder metoderna Node och CompositeNode för att ta bort ett avsnitt före det sista avsnittet i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Båda sektionerna är syskon till varandra.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Ta bort en sektion baserat på dess syskonrelation med en annan sektion.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// Avsnittet vi tog bort var det första, vilket lämnade dokumentet med bara det andra.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### Se även

* class [Node](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
