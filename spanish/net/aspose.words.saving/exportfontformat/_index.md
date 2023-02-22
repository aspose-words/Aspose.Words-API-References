---
title: Enum ExportFontFormat
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.ExportFontFormat enumeración. Indica el formato que se utiliza para exportar fuentes mientras se renderiza a formato HTML fijo.
type: docs
weight: 4730
url: /es/net/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enumeration

Indica el formato que se utiliza para exportar fuentes mientras se renderiza a formato HTML fijo.

```csharp
public enum ExportFontFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Woff | `0` | WOFF (formato de fuente abierta web). |
| Ttf | `1` | TTF (formato de fuente TrueType). |

### Ejemplos

Muestra cómo usar fuentes solo de la máquina de destino al guardar un documento en HTML.

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


