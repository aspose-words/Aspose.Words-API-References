---
title: StructuredDocumentTagRangeStart.Accept
second_title: Aspose.Words för .NET API Referens
description: StructuredDocumentTagRangeStart metod. Accepterar en besökare.
type: docs
weight: 190
url: /sv/net/aspose.words.markup/structureddocumenttagrangestart/accept/
---
## StructuredDocumentTagRangeStart.Accept method

Accepterar en besökare.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| visitor | DocumentVisitor | Besökaren som kommer att besöka noderna. |

### Returvärde

Sant om alla noder besöktes; falskt om[`DocumentVisitor`](../../../aspose.words/documentvisitor/) stoppade operationen innan du besökte alla noder.

### Anmärkningar

Räknar upp denna nod och alla dess barn. Varje nod anropar en motsvarande metod[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

För mer information se Visitor design mönster.

### Se även

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTagRangeStart](../)
* namnutrymme [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* hopsättning [Aspose.Words](../../../)


