---
title: StructuredDocumentTagRangeEnd.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words für .NET
description: StructuredDocumentTagRangeEnd Accept methode. Akzeptiert einen Besucher in C#.
type: docs
weight: 40
url: /de/net/aspose.words.markup/structureddocumenttagrangeend/accept/
---
## StructuredDocumentTagRangeEnd.Accept method

Akzeptiert einen Besucher.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| visitor | DocumentVisitor | Der Besucher, der die Knoten besucht. |

### Rückgabewert

True, wenn alle Knoten besucht wurden; falsch wenn[`DocumentVisitor`](../../../aspose.words/documentvisitor/) stoppte den Vorgang, bevor alle Knoten besucht wurden.

## Bemerkungen

Listet diesen Knoten und alle seine untergeordneten Knoten auf. Jeder Knoten ruft eine entsprechende Methode auf[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

### Siehe auch

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTagRangeEnd](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
