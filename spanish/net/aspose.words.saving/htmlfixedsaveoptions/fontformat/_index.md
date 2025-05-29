---
title: HtmlFixedSaveOptions.FontFormat
linktitle: FontFormat
articleTitle: FontFormat
second_title: Aspose.Words para .NET
description: Descubra la propiedad HtmlFixedSaveOptions FontFormat para personalizar la exportación de fuentes. Configure y optimice fácilmente su formato predeterminado a Woff para un mejor rendimiento.
type: docs
weight: 90
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/fontformat/
---
## HtmlFixedSaveOptions.FontFormat property

Obtiene o establece[`ExportFontFormat`](../../exportfontformat/) Se utiliza para exportar fuentes. El valor predeterminado esWoff .

```csharp
public ExportFontFormat FontFormat { get; set; }
```

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

* enum [ExportFontFormat](../../exportfontformat/)
* class [HtmlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
