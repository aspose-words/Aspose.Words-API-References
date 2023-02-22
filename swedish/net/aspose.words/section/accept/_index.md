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

Sant om alla noder besöktes; false om DocumentVisitor stoppade operationen innan alla noder besöktes.

### Anmärkningar

Räknar upp denna nod och alla dess barn. Varje nod anropar en motsvarande metod på DocumentVisitor.

För mer information se Visitor design mönster.

Anropar DocumentVisitor.VisitSectionStart, anropar sedan Acceptera för alla underordnade noder i section och anropar DocumentVisitor.VisitSectionEnd i slutet.

### Se även

* class [DocumentVisitor](../../documentvisitor/)
* class [Section](../)
* namnutrymme [Aspose.Words](../../section/)
* hopsättning [Aspose.Words](../../../)


