---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
linktitle: UseTargetMachineFonts
articleTitle: UseTargetMachineFonts
second_title: Aspose.Words for .NET
description: Discover how the UseTargetMachineFonts property in HtmlFixedSaveOptions enhances document display by utilizing target machine fonts. Optimize your font management today!
type: docs
weight: 210
url: /net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to `true`, [`FontFormat`](../fontformat/) and [`ExportEmbeddedFonts`](../exportembeddedfonts/) properties do not have effect, also [`ResourceSavingCallback`](../resourcesavingcallback/) is not fired for fonts. Default is `false`.

```csharp
public bool UseTargetMachineFonts { get; set; }
```

## Examples

Shows how use fonts only from the target machine when saving a document to HTML.

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
    Assert.That(Regex.Match(outDocContents, "@font-face").Success, Is.False);
else
    Assert.That(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], " +
        "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }").Success, Is.True);
```

### See Also

* class [HtmlFixedSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
