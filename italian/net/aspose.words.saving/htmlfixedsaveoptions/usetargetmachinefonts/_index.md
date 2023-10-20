---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
linktitle: UseTargetMachineFonts
articleTitle: UseTargetMachineFonts
second_title: Aspose.Words per .NET
description: HtmlFixedSaveOptions UseTargetMachineFonts proprietà. Il flag indica se è necessario utilizzare i caratteri del computer di destinazione per visualizzare il documento. Se questo flag è impostato suVERO FontFormat EExportEmbeddedFonts le proprietà non hanno effetto ancheResourceSavingCallback non viene attivato per i caratteri. Limpostazione predefinita èfalso  in C#.
type: docs
weight: 190
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

Il flag indica se è necessario utilizzare i caratteri del computer di destinazione per visualizzare il documento. Se questo flag è impostato su`VERO` ,[`FontFormat`](../fontformat/) E[`ExportEmbeddedFonts`](../exportembeddedfonts/) le proprietà non hanno effetto, anche[`ResourceSavingCallback`](../resourcesavingcallback/) non viene attivato per i caratteri. L'impostazione predefinita è`falso` .

```csharp
public bool UseTargetMachineFonts { get; set; }
```

## Esempi

Mostra come utilizzare i caratteri solo dal computer di destinazione quando si salva un documento in HTML.

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

### Guarda anche

* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
