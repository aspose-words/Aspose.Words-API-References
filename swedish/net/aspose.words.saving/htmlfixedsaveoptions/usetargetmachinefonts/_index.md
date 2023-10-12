---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
second_title: Aspose.Words för .NET API Referens
description: HtmlFixedSaveOptions fast egendom. Flagga indikerar om teckensnitt från måldatorn måste användas för att visa dokumentet. Om denna flagga är inställd påSann FontFormat ochExportEmbeddedFonts egenskaper har ingen effekt ocksåResourceSavingCallback aktiveras inte för teckensnitt. Standard ärfalsk .
type: docs
weight: 190
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

Flagga indikerar om teckensnitt från måldatorn måste användas för att visa dokumentet. Om denna flagga är inställd på`Sann` ,[`FontFormat`](../fontformat/) och[`ExportEmbeddedFonts`](../exportembeddedfonts/) egenskaper har ingen effekt, också[`ResourceSavingCallback`](../resourcesavingcallback/) aktiveras inte för teckensnitt. Standard är`falsk` .

```csharp
public bool UseTargetMachineFonts { get; set; }
```

### Exempel

Visar hur teckensnitt endast används från målmaskinen när du sparar ett dokument i HTML.

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
* namnutrymme [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* hopsättning [Aspose.Words](../../../)


