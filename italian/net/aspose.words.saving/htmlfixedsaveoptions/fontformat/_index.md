---
title: HtmlFixedSaveOptions.FontFormat
second_title: Aspose.Words per .NET API Reference
description: HtmlFixedSaveOptions proprietà. Ottiene o impostaExportFontFormat utilizzato per lesportazione dei caratteri. Il valore predefinito èWoff .
type: docs
weight: 90
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/fontformat/
---
## HtmlFixedSaveOptions.FontFormat property

Ottiene o imposta[`ExportFontFormat`](../../exportfontformat/) utilizzato per l'esportazione dei caratteri. Il valore predefinito èWoff .

```csharp
public ExportFontFormat FontFormat { get; set; }
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

* enum [ExportFontFormat](../../exportfontformat/)
* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* assemblea [Aspose.Words](../../../)


