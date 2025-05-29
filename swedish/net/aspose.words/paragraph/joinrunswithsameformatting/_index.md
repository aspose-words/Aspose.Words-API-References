---
title: Paragraph.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words för .NET
description: Koppla enkelt samman stycken med konsekvent formatering i dina stycken med hjälp av metoden JoinRunsWithSameFormatting. Förbättra ditt dokuments stil idag!
type: docs
weight: 300
url: /sv/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

Kopplar samman körningar med samma formatering i stycket.

```csharp
public int JoinRunsWithSameFormatting()
```

### Returvärde

Antal utförda kopplingar. När**N** angränsande löpningar sammanfogas räknas de som**N-1** ansluter sig.

## Exempel

Visar hur man förenklar stycken genom att sammanfoga överflödiga stycken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga fyra textsekvenser i stycket.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// Om vi öppnar det här dokumentet i Microsoft Word kommer stycket att se ut som en enda sömlös text.
// Den kommer dock att bestå av fyra separata körningar med samma formatering. Fragmenterade stycken som detta
// kan uppstå när vi manuellt redigerar delar av ett stycke många gånger i Microsoft Word.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// Ändra stilen på den sista körningen för att skilja den från de tre första.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// Vi kan köra metoden "JoinRunsWithSameFormatting" för att optimera dokumentets innehåll
// genom att slå samman liknande körningar till en, vilket minskar deras totala antal.
// Denna metod returnerar också antalet körningar som metoden har sammanfogat.
// Dessa två sammanslagningar skedde för att kombinera körningar #1, #2 och #3,
// samtidigt som man utelämnar körning #4 eftersom den har en inkompatibel stil.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// Antalet återstående körningar kommer att vara lika med det ursprungliga antalet
// minus antalet körningar som sammanslagningar utfördes av metoden "JoinRunsWithSameFormatting".
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### Se även

* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
