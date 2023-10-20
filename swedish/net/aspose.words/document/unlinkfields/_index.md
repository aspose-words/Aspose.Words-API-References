---
title: Document.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words för .NET
description: Document UnlinkFields metod. Tar bort länkar till fält i hela dokumentet i C#.
type: docs
weight: 730
url: /sv/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

Tar bort länkar till fält i hela dokumentet.

```csharp
public void UnlinkFields()
```

## Anmärkningar

Ersätter alla fält i hela dokumentet med deras senaste resultat.

För att ta bort länkar till fält i en specifik del av dokumentet använd[`UnlinkFields`](../../range/unlinkfields/).

## Exempel

Visar hur man tar bort länken till alla fält i dokumentet.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

doc.UnlinkFields();
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
