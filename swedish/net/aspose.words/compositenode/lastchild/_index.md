---
title: CompositeNode.LastChild
linktitle: LastChild
articleTitle: LastChild
second_title: Aspose.Words för .NET
description: CompositeNode LastChild fast egendom. Hämtar nodens sista underordnade i C#.
type: docs
weight: 50
url: /sv/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

Hämtar nodens sista underordnade.

```csharp
public Node LastChild { get; }
```

## Anmärkningar

Om det inte finns någon sista underordnad nod, a`null` returneras.

## Exempel

Visar hur man använder metoderna för Node och CompositeNode för att ta bort ett avsnitt före det sista avsnittet i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// Båda sektionerna är syskon till varandra.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// Ta bort ett avsnitt baserat på dess syskonförhållande med ett annat avsnitt.
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
