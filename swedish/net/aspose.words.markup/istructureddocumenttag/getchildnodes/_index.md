---
title: IStructuredDocumentTag.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words för .NET
description: Upptäck metoden IStructuredDocumentTag GetChildNodes och få tillgång till en dynamisk samling av underordnade noder anpassade till dina angivna typer för förbättrad dokumenthantering.
type: docs
weight: 170
url: /sv/net/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag.GetChildNodes method

Returnerar en live-samling av underordnade noder som matchar de angivna typerna.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

## Exempel

Visar hur man tar bort taggen för strukturerat dokument, men behåller innehållet inuti.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // Denna samling tillhandahåller ett enhetligt gränssnitt för åtkomst till strukturerade taggar med och utan intervall.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Här kan vi hämta underordnade noder från det gemensamma gränssnittet för strukturerade taggar med och utan intervall.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Se även

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* interface [IStructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
