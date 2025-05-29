---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
linktitle: UseTargetMachineFonts
articleTitle: UseTargetMachineFonts
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft UseTargetMachineFonts in HtmlFixedSaveOptions die Dokumentanzeige durch die Verwendung von Zielmaschinenschriften verbessert. Optimieren Sie noch heute Ihr Schriftmanagement!
type: docs
weight: 210
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

Flag gibt an, ob Schriftarten vom Zielcomputer zur Anzeige des Dokuments verwendet werden müssen. Wenn dieses Flag auf`WAHR` ,[`FontFormat`](../fontformat/) Und[`ExportEmbeddedFonts`](../exportembeddedfonts/) Eigenschaften haben keine Wirkung, auch[`ResourceSavingCallback`](../resourcesavingcallback/) wird nicht für Schriftarten ausgelöst. Standard ist`FALSCH` .

```csharp
public bool UseTargetMachineFonts { get; set; }
```

## Beispiele

Zeigt, wie beim Speichern eines Dokuments im HTML-Format nur Schriftarten vom Zielcomputer verwendet werden.

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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
