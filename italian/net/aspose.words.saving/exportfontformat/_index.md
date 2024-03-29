---
title: ExportFontFormat Enum
linktitle: ExportFontFormat
articleTitle: ExportFontFormat
second_title: Aspose.Words per .NET
description: Aspose.Words.Saving.ExportFontFormat enum. Indica il formato utilizzato per esportare i caratteri durante il rendering nel formato fisso HTML in C#.
type: docs
weight: 4990
url: /it/net/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enumeration

Indica il formato utilizzato per esportare i caratteri durante il rendering nel formato fisso HTML.

```csharp
public enum ExportFontFormat
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Woff | `0` | WOFF (formato carattere aperto Web). |
| Ttf | `1` | TTF (formato carattere TrueType). |

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

* property [FontFormat](../htmlfixedsaveoptions/fontformat/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
