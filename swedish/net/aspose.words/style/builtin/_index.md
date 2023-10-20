---
title: Style.BuiltIn
linktitle: BuiltIn
articleTitle: BuiltIn
second_title: Aspose.Words för .NET
description: Style BuiltIn fast egendom. Sant om denna stil är en av de inbyggda stilarna i MS Word i C#.
type: docs
weight: 40
url: /sv/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

Sant om denna stil är en av de inbyggda stilarna i MS Word.

```csharp
public bool BuiltIn { get; }
```

## Exempel

Visar hur man kan skilja anpassade stilar från inbyggda stilar.

```csharp
Document doc = new Document();

// När vi skapar ett dokument med Microsoft Word eller programmatiskt med Aspose.Words,
// dokumentet kommer med en samling stilar att tillämpa på dess text för att ändra dess utseende.
// Vi kan komma åt dessa inbyggda stilar via dokumentets "Styles"-samling.
// Dessa stilar kommer alla att ha flaggan "BuiltIn" inställd på "true".
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// Skapa en anpassad stil och lägg till den i samlingen.
// Anpassade stilar som denna kommer att ha "BuiltIn"-flaggan inställd på "false".
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### Se även

* class [Style](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
