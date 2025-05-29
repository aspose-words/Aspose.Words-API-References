---
title: ExportFontFormat Enum
linktitle: ExportFontFormat
articleTitle: ExportFontFormat
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Saving.ExportFontFormat pour une exportation optimale des polices lors du rendu au format HTML fixe. Améliorez la qualité visuelle de votre document !
type: docs
weight: 5740
url: /fr/net/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enumeration

Indique le format utilisé pour exporter les polices lors du rendu au format fixe HTML.

```csharp
public enum ExportFontFormat
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Woff | `0` | WOFF (format de police Web Open). |
| Ttf | `1` | TTF (format de police TrueType). |

## Exemples

Montre comment utiliser uniquement les polices de la machine cible lors de l'enregistrement d'un document au format HTML.

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

### Voir également

* property [FontFormat](../htmlfixedsaveoptions/fontformat/)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
