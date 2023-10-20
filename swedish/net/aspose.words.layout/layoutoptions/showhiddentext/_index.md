---
title: LayoutOptions.ShowHiddenText
linktitle: ShowHiddenText
articleTitle: ShowHiddenText
second_title: Aspose.Words för .NET
description: LayoutOptions ShowHiddenText fast egendom. Hämtar eller ställer in en indikation på om dold text i dokumentet renderas. Standard ärfalsk  i C#.
type: docs
weight: 80
url: /sv/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

Hämtar eller ställer in en indikation på om dold text i dokumentet renderas. Standard är`falsk` .

```csharp
public bool ShowHiddenText { get; set; }
```

## Anmärkningar

Den här egenskapen påverkar allt dolt innehåll, inte bara text.

## Exempel

Visar hur man döljer text i ett renderat utdatadokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Infoga dold text och ange sedan om vi vill utelämna den från ett renderat dokument.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

### Se även

* class [LayoutOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
