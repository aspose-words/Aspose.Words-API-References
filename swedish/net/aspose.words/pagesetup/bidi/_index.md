---
title: PageSetup.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words för .NET
description: Upptäck PageSetup Bidi-egenskapen för sömlös dubbelriktad textformatering. Förbättra dina dokument med stöd för komplexa skript för bättre läsbarhet!
type: docs
weight: 10
url: /sv/net/aspose.words/pagesetup/bidi/
---
## PageSetup.Bidi property

Anger att det här avsnittet innehåller dubbelriktad text (komplexa skript).

```csharp
public bool Bidi { get; set; }
```

## Anmärkningar

När`sann`, kolumnerna i det här avsnittet är upplagda från höger till vänster.

## Exempel

Visar hur man ställer in ordningen på textkolumner i ett avsnitt.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextColumns.SetCount(3);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 3.");

// Sätt egenskapen "Bidi" till "true" för att ordna kolumnerna med början från sidans högra sida.
// Kolumnernas ordning kommer att matcha riktningen på texten från höger till vänster.
// Sätt egenskapen "Bidi" till "false" för att ordna kolumnerna med början från sidans vänstra sida.
// Kolumnernas ordning matchar riktningen på texten från vänster till höger.
pageSetup.Bidi = reverseColumns;

doc.Save(ArtifactsDir + "PageSetup.Bidi.docx");
```

### Se även

* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
