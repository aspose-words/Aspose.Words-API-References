---
title: ExportFontFormat Enum
linktitle: ExportFontFormat
articleTitle: ExportFontFormat
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Saving.ExportFontFormat per un'esportazione ottimale dei font durante il rendering in formato HTML fisso. Migliora la qualità visiva del tuo documento!
type: docs
weight: 5740
url: /it/net/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enumeration

Indica il formato utilizzato per esportare i font durante il rendering nel formato fisso HTML.

```csharp
public enum ExportFontFormat
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Woff | `0` | WOFF (formato di font Web aperto). |
| Ttf | `1` | TTF (formato carattere TrueType). |

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

* property [FontFormat](../htmlfixedsaveoptions/fontformat/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
