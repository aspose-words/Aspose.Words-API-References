---
title: Font.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words för .NET
description: Font Style fast egendom. Hämtar eller ställer in teckenstilen som tillämpas på denna formatering i C#.
type: docs
weight: 400
url: /sv/net/aspose.words/font/style/
---
## Font.Style property

Hämtar eller ställer in teckenstilen som tillämpas på denna formatering.

```csharp
public Style Style { get; set; }
```

## Exempel

Tillämpar en dubbel understrykning på alla körningar i ett dokument som är formaterade med anpassade teckenstilar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en anpassad stil och tillämpa den på text som skapats med ett dokumentbyggare.
Style style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Red;
style.Font.Name = "Courier New";

builder.Font.StyleName = "MyStyle";
builder.Write("This text is in a custom style.");

// Iterera över varje körning och lägg till en dubbel understrykning till varje anpassad stil.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
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
