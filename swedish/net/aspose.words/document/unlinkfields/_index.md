---
title: Document.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words för .NET
description: Upptäck hur du använder metoden UnlinkFields för att effektivt koppla bort länkar från fält i hela dokumentet, vilket förbättrar ditt redigeringsarbetsflöde.
type: docs
weight: 780
url: /sv/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

Avlänkar fält i hela dokumentet.

```csharp
public void UnlinkFields()
```

## Anmärkningar

Ersätter alla fält i hela dokumentet med deras senaste resultat.

För att koppla bort länkar från fält i en specifik del av dokumentet, använd[`UnlinkFields`](../../range/unlinkfields/).

## Exempel

Visar hur man tar bort länkar från alla fält i dokumentet.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

doc.UnlinkFields();
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
