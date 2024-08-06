---
title: ExportFontFormat Enum
linktitle: ExportFontFormat
articleTitle: ExportFontFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.ExportFontFormat enum. Indicates the format that is used to export fonts while rendering to HTML fixed format in C#.
type: docs
weight: 5290
url: /net/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enumeration

Indicates the format that is used to export fonts while rendering to HTML fixed format.

```csharp
public enum ExportFontFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Woff | `0` | WOFF (Web Open Font Format). |
| Ttf | `1` | TTF (TrueType Font format). |

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
    Assert.False(Regex.Match(outDocContents, "@font-face").Success);
else
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], " +
        "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }").Success);
```

### See Also

* property [FontFormat](../htmlfixedsaveoptions/fontformat/)
* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
