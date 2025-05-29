---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
linktitle: UseTargetMachineFonts
articleTitle: UseTargetMachineFonts
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen UseTargetMachineFonts i HtmlFixedSaveOptions förbättrar dokumentvisningen genom att använda målmaskinens teckensnitt. Optimera din teckensnittshantering idag!
type: docs
weight: 210
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

Flaggan anger om teckensnitt från måldatorn måste användas för att visa dokumentet. Om denna flagga är inställd på`sann` ,[`FontFormat`](../fontformat/) och[`ExportEmbeddedFonts`](../exportembeddedfonts/) egenskaper har ingen effekt, också[`ResourceSavingCallback`](../resourcesavingcallback/) aktiveras inte för teckensnitt. Standard är`falsk` .

```csharp
public bool UseTargetMachineFonts { get; set; }
```

## Exempel

Visar hur man endast använder teckensnitt från måldatorn när man sparar ett dokument till HTML.

```csharp
Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = true,
    UseTargetMachineFonts = useTargetMachineFonts,
    FontFormat = ExportFontFormat.Ttf,
    ExportEmbeddedFonts = false,
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
    Assert.False(Regex.Match(outDocContents, "@font-face").Success);
else
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], " +
        "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }").Success);
```

### Se även

* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
