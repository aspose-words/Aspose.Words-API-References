---
title: LayoutOptions.ShowHiddenText
linktitle: ShowHiddenText
articleTitle: ShowHiddenText
second_title: Aspose.Words för .NET
description: Upptäck LayoutOptions ShowHiddenText-egenskapen och styr enkelt renderingen av dold text i dina dokument. Optimera din innehålls synlighet idag!
type: docs
weight: 80
url: /sv/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

Hämtar eller anger om dold text i dokumentet renderas. Standard är`falsk` .

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
