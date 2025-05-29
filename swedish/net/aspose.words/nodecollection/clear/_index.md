---
title: NodeCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words för .NET
description: Rensa enkelt din NodeCollection med vår Clear-metod, och ta bort alla noder från både samlingen och dokumentet för optimal prestanda.
type: docs
weight: 40
url: /sv/net/aspose.words/nodecollection/clear/
---
## NodeCollection.Clear method

Tar bort alla noder från den här samlingen och från dokumentet.

```csharp
public void Clear()
```

## Exempel

Visar hur man tar bort alla avsnitt från ett dokument.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Detta dokument har en sektion med några underordnade noder som innehåller och visar dokumentets hela innehåll.
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// Rensa samlingen av sektioner, vilket tar bort alla dokumentets underordnade objekt.
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Se även

* class [NodeCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
