---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words para .NET
description: HtmlFixedSaveOptions ExportEmbeddedImages propiedad. Especifica si las imágenes deben incrustarse en un documento HTML en formato Base64. Tenga en cuenta que configurar este indicador puede aumentar significativamente el tamaño del archivo HTML de salida en C#.
type: docs
weight: 60
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

Especifica si las imágenes deben incrustarse en un documento HTML en formato Base64. Tenga en cuenta que configurar este indicador puede aumentar significativamente el tamaño del archivo HTML de salida.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## Ejemplos

Muestra cómo determinar dónde almacenar imágenes al exportar un documento a HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Cuando exportamos un documento con imágenes incrustadas a .html,
// Aspose.Words puede colocar las imágenes en dos ubicaciones posibles.
// Establecer el indicador "ExportEmbeddedImages" en "true" almacenará los datos sin procesar
// para todas las imágenes dentro del documento HTML de salida, en el atributo "src" de <image> etiquetas.
// Establecer este indicador en "falso" creará un archivo de imagen en el sistema de archivos local para cada imagen,
// y almacena todos estos archivos en una carpeta separada.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedImages = exportImages
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" " +
        "src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />").Success);
}
```

### Ver también

* class [HtmlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
