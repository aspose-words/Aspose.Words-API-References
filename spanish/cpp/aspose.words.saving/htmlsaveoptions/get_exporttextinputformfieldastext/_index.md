---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText método"
linktitle: "get_ExportTextInputFormFieldAsText"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText método. Controla cómo se guardan los campos de formulario de entrada de texto en HTML o MHTML. El valor predeterminado es false en C++."
type: docs
weight: 28000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exporttextinputformfieldastext/
---
## HtmlSaveOptions::get_ExportTextInputFormFieldAsText method


Controla cómo se guardan los campos de formulario de entrada de texto en HTML o MHTML. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText() const
```

## Observaciones


Cuando se establece en **true**, exporta los campos de formulario de entrada de texto como texto normal. Cuando se establece en **false**, exporta los campos de formulario de texto de Word como elementos INPUT en HTML.

Al exportar a EPUB, los campos de formulario de entrada de texto siempre se guardan como texto debido a los requisitos de este formato.

## Ejemplos



Muestra cómo especificar la carpeta para almacenar imágenes vinculadas después de guardar en .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Establece una opción para exportar los campos de formulario como texto plano en lugar de elementos de entrada HTML.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
