---
title: StructuredDocumentTagRangeEnd.Accept
second_title: Aspose.Words för .NET API Referens
description: StructuredDocumentTagRangeEnd metod. Accepterar en besökare.
type: docs
weight: 40
url: /sv/net/aspose.words.markup/structureddocumenttagrangeend/accept/
---
## StructuredDocumentTagRangeEnd.Accept method

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
* class [StructuredDocumentTagRangeEnd](../)
* namnutrymme [Aspose.Words.Markup](../../structureddocumenttagrangeend/)
* hopsättning [Aspose.Words](../../../)


