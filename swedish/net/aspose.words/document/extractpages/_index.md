---
title: Document.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words för .NET
description: Upptäck Document ExtractPages-metoden för att enkelt hämta specifika sidintervall, vilket förbättrar din dokumenthantering och effektivitet.
type: docs
weight: 640
url: /sv/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

Returnerar[`Document`](../) objekt som representerar ett angivet sidintervall.

```csharp
public Document ExtractPages(int index, int count)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | Int32 | Det nollbaserade indexet för den första sidan som ska extraheras. |
| count | Int32 | Antal sidor som ska extraheras. |

## Anmärkningar

Det resulterande dokumentet ska se ut som det i MS Word, som om vi hade utfört "Skriv ut specifika sidor" – numreringen, sidhuvuden/sidfötter och layouten för korstabeller kommer att behållas. Men på grund av ett stort antal nyanser, som uppstår när antalet sidor minskas, är fullständig matchning av layouten en ganska komplicerad uppgift som kräver mycket ansträngning. Beroende på dokumentets komplexitet kan det finnas små skillnader i layouten för det resulterande dokumentinnehållet jämfört med källdokumentet. All feedback uppskattas mycket.

## Exempel

Visar hur man hämtar ett angivet sidintervall från dokumentet.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
