---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages método"
linktitle: "get_ExportEmbeddedImages"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages método. Especifica si las imágenes deben incrustarse en el documento Html en formato Base64. Tenga en cuenta que activar esta bandera puede aumentar significativamente el tamaño del archivo Html de salida en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedimages/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedImages method


Especifica si las imágenes deben incrustarse en el documento Html en formato Base64. Nota: activar esta opción puede aumentar significativamente el tamaño del archivo Html de salida.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages() const
```


## Ejemplos



Muestra cómo determinar dónde almacenar las imágenes al exportar un documento a Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Cuando exportamos un documento con imágenes incrustadas a .html,
// Aspose.Words puede colocar las imágenes en dos ubicaciones posibles.
// Establecer la bandera "ExportEmbeddedImages" a "true" almacenará los datos sin procesar
// para todas las imágenes dentro del documento HTML de salida, en el atributo "src" de las etiquetas <image>.
// Establecer esta bandera a "false" creará un archivo de imagen en el sistema de archivos local para cada imagen,
// y almacenará todos estos archivos en una carpeta separada.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedImages(exportImages);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" ") + u"src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />")->get_Success());
}
```

## Ver también

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
