---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
second_title: Aspose.Words per .NET API Reference
description: HtmlFixedSaveOptions proprietà. Flag indica se i caratteri della macchina di destinazione devono essere utilizzati per visualizzare il documento. Se questo flag è impostato su trueFontFormat eExportEmbeddedFontsle proprietà non hanno effetto anche ResourceSavingCallback non viene attivato per i caratteri. Limpostazione predefinita è false.
type: docs
weight: 190
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

Flag indica se i caratteri della macchina di destinazione devono essere utilizzati per visualizzare il documento. Se questo flag è impostato su true,[`FontFormat`](../fontformat/) e[`ExportEmbeddedFonts`](../exportembeddedfonts/)le proprietà non hanno effetto, anche [`ResourceSavingCallback`](../resourcesavingcallback/) non viene attivato per i caratteri. L'impostazione predefinita è false.

```csharp
public bool UseTargetMachineFonts { get; set; }
```

### Esempi

Mostra come utilizzare i font solo dalla macchina di destinazione durante il salvataggio di un documento in HTML.

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
* spazio dei nomi [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* assemblea [Aspose.Words](../../../)


