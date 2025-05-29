---
title: ExportFontFormat Enum
linktitle: ExportFontFormat
articleTitle: ExportFontFormat
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Saving.ExportFontFormat para una exportación óptima de fuentes al renderizar a formato HTML fijo. ¡Mejore la calidad visual de su documento!
type: docs
weight: 5740
url: /es/net/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enumeration

Indica el formato que se utiliza para exportar fuentes mientras se renderiza en formato fijo HTML.

```csharp
public enum ExportFontFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Woff | `0` | WOFF (Formato de fuente abierto para web). |
| Ttf | `1` | TTF (formato de fuente TrueType). |

## Ejemplos

Muestra cómo utilizar únicamente fuentes de la máquina de destino al guardar un documento en HTML.

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

### Ver también

* property [FontFormat](../htmlfixedsaveoptions/fontformat/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
