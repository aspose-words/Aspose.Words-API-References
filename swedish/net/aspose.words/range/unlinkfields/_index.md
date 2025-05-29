---
title: Range.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words för .NET
description: Upptäck metoden Range UnlinkFields för att enkelt koppla bort länkar från fält i ditt dokumentintervall, vilket förbättrar ditt arbetsflöde och din dokumenthantering.
type: docs
weight: 120
url: /sv/net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

Avlänkar fält i detta intervall.

```csharp
public void UnlinkFields()
```

## Anmärkningar

Ersätter alla fält i detta intervall med deras senaste resultat.

För att koppla bort länkar från fält i hela dokumentet, använd`UnlinkFields`.

## Exempel

Visar hur man tar bort länkar från alla fält i ett område.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

Section newSection = (Section)doc.Sections[0].Clone(true);
doc.Sections.Add(newSection);

doc.Sections[1].Range.UnlinkFields();
```

### Se även

* class [Range](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
