---
title: CompositeNode.LastChild
second_title: Aspose.Words för .NET API Referens
description: CompositeNode fast egendom. Hämtar nodens sista underordnade.
type: docs
weight: 60
url: /sv/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

Hämtar nodens sista underordnade.

```csharp
public Node LastChild { get; }
```

### Anmärkningar

Om det inte finns någon sista underordnad nod returneras en noll.

### Exempel

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
* namnutrymme [Aspose.Words](../../compositenode/)
* hopsättning [Aspose.Words](../../../)


