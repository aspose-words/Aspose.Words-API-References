---
title: CompositeNode.RemoveChild
linktitle: RemoveChild
articleTitle: RemoveChild
second_title: Aspose.Words för .NET
description: Hantera enkelt din CompositeNode med RemoveChild-metoden, utformad för att effektivisera borttagning av nod för förbättrad prestanda och effektivitet.
type: docs
weight: 190
url: /sv/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild&lt;T&gt; method

Tar bort den angivna undernoden.

```csharp
public T RemoveChild<T>(T oldChild)
    where T : Node
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| oldChild | T | Noden som ska tas bort. |

### Returvärde

Den borttagna noden.

## Anmärkningar

Föräldern till*oldChild* är inställd på`null` efter att noden har tagits bort.

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
