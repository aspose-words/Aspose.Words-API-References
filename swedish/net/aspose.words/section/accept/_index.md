---
title: Section.Accept
second_title: Aspose.Words för .NET API Referens
description: Section metod. Accepterar en besökare.
type: docs
weight: 70
url: /sv/net/aspose.words/section/accept/
---
## Section.Accept method

Accepterar en besökare.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| visitor | DocumentVisitor | Besökaren som kommer att besöka noderna. |

### Returvärde

Sant om alla noder besöktes; falskt om[`DocumentVisitor`](../../documentvisitor/) stoppade operationen innan du besökte alla noder.

### Anmärkningar

Räknar upp denna nod och alla dess barn. Varje nod anropar en motsvarande metod[`DocumentVisitor`](../../documentvisitor/).

För mer information se Visitor design mönster.

Samtal[`VisitSectionStart`](../../documentvisitor/visitsectionstart/) , sedan ringer[`Accept`](../../node/accept/) för alla underordnade noder i avsnittet och anrop[`VisitSectionEnd`](../../documentvisitor/visitsectionend/) i slutet.

### Se även

* class [DocumentVisitor](../../documentvisitor/)
* class [Section](../)
* namnutrymme [Aspose.Words](../../section/)
* hopsättning [Aspose.Words](../../../)


