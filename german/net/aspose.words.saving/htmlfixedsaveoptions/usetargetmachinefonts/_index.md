---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlFixedSaveOptions eigendom. Flag gibt an ob Schriftarten vom Zielcomputer verwendet werden müssen um das Dokument anzuzeigen. Wenn dieses Flag auf true gesetzt istFontFormat undExportEmbeddedFontsEigenschaften haben keine Wirkung auchResourceSavingCallback wird nicht für Schriftarten ausgelöst. Standard ist falsch.
type: docs
weight: 190
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

Flag gibt an, ob Schriftarten vom Zielcomputer verwendet werden müssen, um das Dokument anzuzeigen. Wenn dieses Flag auf true gesetzt ist,[`FontFormat`](../fontformat/) und[`ExportEmbeddedFonts`](../exportembeddedfonts/)Eigenschaften haben keine Wirkung, auch[`ResourceSavingCallback`](../resourcesavingcallback/) wird nicht für Schriftarten ausgelöst. Standard ist falsch.

```csharp
public bool UseTargetMachineFonts { get; set; }
```

### Beispiele

Zeigt, wie Schriftarten nur vom Zielcomputer verwendet werden, wenn ein Dokument in HTML gespeichert wird.

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

### Siehe auch

* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* Montage [Aspose.Words](../../../)


