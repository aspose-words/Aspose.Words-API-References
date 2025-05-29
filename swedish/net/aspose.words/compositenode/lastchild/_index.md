---
title: CompositeNode.LastChild
linktitle: LastChild
articleTitle: LastChild
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CompositeNode LastChild för att enkelt komma åt och manipulera den sista underordnade noden, vilket förbättrar din datastrukturhantering.
type: docs
weight: 50
url: /sv/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

Hämtar nodens sista barn.

```csharp
public Node LastChild { get; }
```

## Anmärkningar

Om det inte finns någon sista underordnad nod, en`null` returneras.

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

* class [Node](../../node/)
* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
