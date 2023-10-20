---
title: Document.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words för .NET
description: Document ExtractPages metod. ReturnerarDocument objekt som representerar specificerat intervall av sidor i C#.
type: docs
weight: 600
url: /sv/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

Returnerar[`Document`](../) objekt som representerar specificerat intervall av sidor.

```csharp
public Document ExtractPages(int index, int count)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | Int32 | Det nollbaserade indexet för den första sidan som ska extraheras. |
| count | Int32 | Antal sidor som ska extraheras. |

## Anmärkningar

Det resulterande dokumentet ska se ut som det i MS Word, som om vi hade utfört 'Skriv ut specifika sidor' – numreringen, sidhuvuden/sidfötter och korstabelllayouten kommer att bevaras. Men på grund av ett stort antal nyanser, visas samtidigt som man minskar antalet sidor, är fullständig matchning av layouten en tyst och komplicerad uppgift som kräver mycket ansträngning. Beroende på dokumentets komplexitet kan det finnas små skillnader i den resulterande dokumentinnehållslayouten jämfört med källdokumentet. All feedback skulle vara mycket uppskattad.

## Exempel

Visar hur man får specificerat sidintervall från dokumentet.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
