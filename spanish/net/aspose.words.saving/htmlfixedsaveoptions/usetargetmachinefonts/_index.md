---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
linktitle: UseTargetMachineFonts
articleTitle: UseTargetMachineFonts
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad UseTargetMachineFonts de HtmlFixedSaveOptions mejora la visualización del documento al utilizar las fuentes de la máquina de destino. ¡Optimice su gestión de fuentes hoy mismo!
type: docs
weight: 210
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

El indicador indica si se deben usar las fuentes de la máquina de destino para mostrar el documento. Si este indicador está configurado en`verdadero` ,[`FontFormat`](../fontformat/) y[`ExportEmbeddedFonts`](../exportembeddedfonts/) las propiedades no tienen efecto, también[`ResourceSavingCallback`](../resourcesavingcallback/) no se activa para fuentes. El valor predeterminado es`FALSO` .

```csharp
public bool UseTargetMachineFonts { get; set; }
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

* class [HtmlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
