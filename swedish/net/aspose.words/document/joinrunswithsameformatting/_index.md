---
title: Document.JoinRunsWithSameFormatting
second_title: Aspose.Words för .NET API Referens
description: Document metod. Sammanfogar körningar med samma formatering i alla stycken i dokumentet.
type: docs
weight: 600
url: /sv/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

Sammanfogar körningar med samma formatering i alla stycken i dokumentet.

```csharp
public int JoinRunsWithSameFormatting()
```

### Returvärde

Antal utförda anslutningar. När **N** angränsande körningar sammanfogas de räknas som **N - 1** ansluter sig.

### Anmärkningar

Detta är en optimeringsmetod. Vissa dokument innehåller angränsande körningar med samma formatering. Vanligtvis inträffar detta om ett dokument har redigerats intensivt manuellt. Du kan minska dokumentstorleken och påskynda ytterligare bearbetning genom att sammanfoga dessa körningar.

Operationen kontrollerar varje[`Paragraph`](../../paragraph/) nod i dokumentet för intilliggande[`Run`](../../run/) noder med identiska egenskaper. Den ignorerar unika identifierare som används för att spåra redigeringssessioner för skapande och modifiering av run . Första körningen i varje sammanfogningssekvens ackumulerar all text. Remaining körningar tas bort från dokumentet.

### Exempel

Visar hur man sammanfogar körningar i ett dokument för att minska onödiga körningar.

```csharp
// Öppna ett dokument som innehåller intilliggande serier av text med identisk formatering,
// vilket ofta inträffar om vi redigerar samma stycke flera gånger i Microsoft Word.
Document doc = new Document(MyDir + "Rendering.docx");

// Om något antal av dessa körningar ligger intill med identisk formatering,
// då kan dokumentet förenklas.
Assert.AreEqual(317, doc.GetChildNodes(NodeType.Run, true).Count);

// Kombinera sådana körningar med den här metoden och verifiera antalet körningar som kommer att äga rum.
Assert.AreEqual(121, doc.JoinRunsWithSameFormatting());

// Antalet anslutningar och antalet körningar vi har efter sammanfogningen
// bör summera antalet körningar vi hade från början.
Assert.AreEqual(196, doc.GetChildNodes(NodeType.Run, true).Count);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


