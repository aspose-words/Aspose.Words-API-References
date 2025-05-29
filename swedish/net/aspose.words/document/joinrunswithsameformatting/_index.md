---
title: Document.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words för .NET
description: Upptäck hur metoden JoinRunsWithSameFormatting sömlöst sammanfogar formaterad text i dokumentets stycken för ett elegant och professionellt utseende.
type: docs
weight: 660
url: /sv/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

Kopplar samman körningar med samma formatering i alla stycken i dokumentet.

```csharp
public int JoinRunsWithSameFormatting()
```

### Returvärde

Antal utförda kopplingar. När**N** angränsande löpningar sammanfogas räknas de som**N-1** ansluter sig.

## Anmärkningar

Detta är en optimeringsmetod. Vissa dokument innehåller intilliggande körningar med samma formatering. Vanligtvis inträffar detta om ett dokument har redigerats intensivt manuellt. Du kan minska dokumentstorleken och påskynda vidare bearbetning genom att sammanfoga dessa körningar.

Operationen kontrollerar varje[`Paragraph`](../../paragraph/) nod i dokumentet för intilliggande[`Run`](../../run/) -noder med identiska egenskaper. Den ignorerar unika identifierare som används för att spåra redigeringssessioner för skapande och modifiering av run . Den första körningen i varje kopplingssekvens ackumulerar all text. Återstående -körningar raderas från dokumentet.

## Exempel

Visar hur man kopplar ihop körningar i ett dokument för att minska onödiga körningar.

```csharp
// Öppna ett dokument som innehåller angränsande textsekvenser med identisk formatering,
// vilket vanligtvis inträffar om vi redigerar samma stycke flera gånger i Microsoft Word.
Document doc = new Document(MyDir + "Rendering.docx");

// Om ett antal av dessa körningar ligger intill varandra med identisk formatering,
// då kan dokumentet förenklas.
Assert.AreEqual(317, doc.GetChildNodes(NodeType.Run, true).Count);

// Kombinera sådana körningar med den här metoden och verifiera antalet körningskopplingar som kommer att äga rum.
Assert.AreEqual(121, doc.JoinRunsWithSameFormatting());

// Antalet joins och antalet körningar vi har efter joinen
// borde lägga ihop antalet körningar vi hade från början.
Assert.AreEqual(196, doc.GetChildNodes(NodeType.Run, true).Count);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
