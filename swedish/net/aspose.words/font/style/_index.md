---
title: Font.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words för .NET
description: Upptäck hur du använder egenskapen Teckensnittsstil för att anpassa teckenstilar i din formatering för att förbättra textens attraktionskraft och läsbarhet.
type: docs
weight: 410
url: /sv/net/aspose.words/font/style/
---
## Font.Style property

Hämtar eller ställer in teckenformatet som tillämpas på denna formatering.

```csharp
public Style Style { get; set; }
```

## Exempel

Använder dubbel understrykning på alla körningar i ett dokument som är formaterade med anpassade teckenformat.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en anpassad stil och tillämpa den på text som skapats med en dokumentbyggare.
Style style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Red;
style.Font.Name = "Courier New";

builder.Font.StyleName = "MyStyle";
builder.Write("This text is in a custom style.");

// Iterera över varje körning och lägg till en dubbel understrykning till varje anpassad stil.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
{
    Style charStyle = run.Font.Style;

    if (!charStyle.BuiltIn)
        run.Font.Underline = Underline.Double;
}

doc.Save(ArtifactsDir + "Font.Style.docx");
```

### Se även

* class [Style](../../style/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
