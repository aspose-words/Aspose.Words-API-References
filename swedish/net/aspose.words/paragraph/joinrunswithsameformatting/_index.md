---
title: Paragraph.JoinRunsWithSameFormatting
second_title: Aspose.Words för .NET API Referens
description: Paragraph metod. Joins körs med samma formatering i stycket.
type: docs
weight: 280
url: /sv/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

Joins körs med samma formatering i stycket.

```csharp
public int JoinRunsWithSameFormatting()
```

### Returvärde

Antal utförda anslutningar. När **N** angränsande körningar sammanfogas de räknas som **N - 1** ansluter sig.

### Exempel

Visar hur man förenklar stycken genom att slå samman överflödiga körningar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga fyra rader text i stycket.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// Om vi öppnar det här dokumentet i Microsoft Word kommer stycket att se ut som en sömlös textkropp.
// Det kommer dock att bestå av fyra separata körningar med samma formatering. Fragmenterade stycken som detta
// kan uppstå när vi manuellt redigerar delar av ett stycke många gånger i Microsoft Word.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// Ändra stilen för den senaste körningen för att skilja den från de tre första.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// Vi kan köra metoden "JoinRunsWithSameFormatting" för att optimera dokumentets innehåll
// genom att slå samman liknande körningar till en, vilket minskar deras totala antal.
// Den här metoden returnerar också antalet körningar som denna metod slog ihop.
// Dessa två sammanslagningar inträffade för att kombinera körningar #1, #2 och #3,
// samtidigt som kör #4 utelämnas eftersom den har en inkompatibel stil.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// Antalet körningar kvar kommer att vara lika med det ursprungliga antalet
// minus antalet körningar som "JoinRunsWithSameFormatting"-metoden utförde.
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### Se även

* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../paragraph/)
* hopsättning [Aspose.Words](../../../)


