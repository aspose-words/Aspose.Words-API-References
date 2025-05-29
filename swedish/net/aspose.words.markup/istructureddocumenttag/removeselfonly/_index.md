---
title: IStructuredDocumentTag.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: Aspose.Words för .NET
description: Upptäck metoden IStructuredDocumentTag RemoveSelfOnly för att enkelt ta bort en SDT-nod samtidigt som innehållet i dokumentträdet bevaras.
type: docs
weight: 180
url: /sv/net/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag.RemoveSelfOnly method

Tar bort endast denna SDT-nod, men behåller dess innehåll i dokumentträdet.

```csharp
public void RemoveSelfOnly()
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

* interface [IStructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
