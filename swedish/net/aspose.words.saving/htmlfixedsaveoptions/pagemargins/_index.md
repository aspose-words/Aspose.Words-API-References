---
title: HtmlFixedSaveOptions.PageMargins
linktitle: PageMargins
articleTitle: PageMargins
second_title: Aspose.Words för .NET
description: HtmlFixedSaveOptions PageMargins fast egendom. Anger marginalerna runt sidor i ett HTMLdokument. Marginalvärdet mäts i punkter och ska vara lika med eller större än 0. Standardvärdet är 10 poäng i C#.
type: docs
weight: 120
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/pagemargins/
---
## HtmlFixedSaveOptions.PageMargins property

Anger marginalerna runt sidor i ett HTML-dokument. Marginalvärdet mäts i punkter och ska vara lika med eller större än 0. Standardvärdet är 10 poäng.

```csharp
public double PageMargins { get; set; }
```

## Anmärkningar

Beror på värdet av[`PageHorizontalAlignment`](../pagehorizontalalignment/) fast egendom:

* Definierar övre, nedre och vänstra sidmarginalerna om värdet ärLeft .
* Definierar övre, nedre och högra sidmarginaler om värdet ärRight .
* Definierar övre och nedre sidmarginaler om värdet ärCenter .

## Exempel

Visar hur du justerar sidmarginalerna när du sparar ett dokument till HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    PageMargins = 15
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins/styles.css");

Assert.True(Regex.Match(outDocContents,
    "[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }").Success);
```

### Se även

* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
