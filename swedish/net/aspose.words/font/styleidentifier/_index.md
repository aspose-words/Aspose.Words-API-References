---
title: Font.StyleIdentifier
second_title: Aspose.Words för .NET API Referens
description: Font fast egendom. Hämtar eller ställer in den språkoberoende stilidentifieraren för teckenstilen som tillämpas på denna formatering.
type: docs
weight: 410
url: /sv/net/aspose.words/font/styleidentifier/
---
## Font.StyleIdentifier property

Hämtar eller ställer in den språkoberoende stilidentifieraren för teckenstilen som tillämpas på denna formatering.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

### Exempel

Visar hur man ändrar stilen på befintlig text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan finns två sätt att referera till stilar.
// 1 - Använd stilnamnet:
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 - Använda en inbyggd stilidentifierare:
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// Konvertera all användning av en stil till en annan,
// använder ovanstående metoder för att referera till gamla och nya stilar.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
{
    if (run.Font.StyleName == "Emphasis")
        run.Font.StyleName = "Strong";

    if (run.Font.StyleIdentifier == StyleIdentifier.IntenseEmphasis)
        run.Font.StyleIdentifier = StyleIdentifier.Strong;
}

doc.Save(ArtifactsDir + "Font.ChangeStyle.docx");
```

### Se även

* enum [StyleIdentifier](../../styleidentifier/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../font/)
* hopsättning [Aspose.Words](../../../)


