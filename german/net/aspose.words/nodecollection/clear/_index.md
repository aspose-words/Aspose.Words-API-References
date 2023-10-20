---
title: NodeCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words für .NET
description: NodeCollection Clear methode. Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument in C#.
type: docs
weight: 40
url: /de/net/aspose.words/nodecollection/clear/
---
## NodeCollection.Clear method

Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument.

```csharp
public void Clear()
```

## Beispiele

Zeigt, wie alle Abschnitte aus einem Dokument entfernt werden.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Dieses Dokument verfügt über einen Abschnitt mit einigen untergeordneten Knoten, die den gesamten Inhalt des Dokuments enthalten und anzeigen.
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// Die Sammlung von Abschnitten löschen, wodurch alle untergeordneten Elemente des Dokuments entfernt werden.
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Siehe auch

* class [NodeCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
