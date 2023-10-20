---
title: Section.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words für .NET
description: Section Accept methode. Akzeptiert einen Besucher in C#.
type: docs
weight: 70
url: /de/net/aspose.words/section/accept/
---
## Section.Accept method

Akzeptiert einen Besucher.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| visitor | DocumentVisitor | Der Besucher, der die Knoten besucht. |

### Rückgabewert

True, wenn alle Knoten besucht wurden; falsch wenn[`DocumentVisitor`](../../documentvisitor/) stoppte den Vorgang, bevor alle Knoten besucht wurden.

## Bemerkungen

Listet diesen Knoten und alle seine untergeordneten Knoten auf. Jeder Knoten ruft eine entsprechende Methode auf[`DocumentVisitor`](../../documentvisitor/).

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

Anrufe[`VisitSectionStart`](../../documentvisitor/visitsectionstart/) , dann ruft[`Accept`](../../node/accept/) für alle untergeordneten Knoten der section und Aufrufe[`VisitSectionEnd`](../../documentvisitor/visitsectionend/) am Ende.

### Siehe auch

* class [DocumentVisitor](../../documentvisitor/)
* class [Section](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
