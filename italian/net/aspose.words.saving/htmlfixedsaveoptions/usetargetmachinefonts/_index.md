---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
linktitle: UseTargetMachineFonts
articleTitle: UseTargetMachineFonts
second_title: Aspose.Words per .NET
description: Scopri come la proprietà UseTargetMachineFonts in HtmlFixedSaveOptions migliora la visualizzazione dei documenti utilizzando i font del computer di destinazione. Ottimizza la gestione dei tuoi font oggi stesso!
type: docs
weight: 210
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

Il flag indica se i font della macchina di destinazione devono essere utilizzati per visualizzare il documento. Se questo flag è impostato su`VERO` ,[`FontFormat`](../fontformat/) E[`ExportEmbeddedFonts`](../exportembeddedfonts/) le proprietà non hanno effetto, anche[`ResourceSavingCallback`](../resourcesavingcallback/) non viene attivato per i font. Il valore predefinito è`falso` .

```csharp
public bool UseTargetMachineFonts { get; set; }
```

## Esempi

Mostra come utilizzare solo i font del computer di destinazione quando si salva un documento in formato HTML.

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
