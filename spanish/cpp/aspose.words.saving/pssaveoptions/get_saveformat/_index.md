---
title: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat método"
linktitle: "get_SaveFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat método. Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo puede ser Ps en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.saving/pssaveoptions/get_saveformat/
---
## PsSaveOptions::get_SaveFormat method


Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo puede ser [Ps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PsSaveOptions::get_SaveFormat() override
```


## Ejemplos



Muestra cómo guardar un documento en formato Postscript en forma de pliegue de libro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Cree un objeto "PsSaveOptions" que podamos pasar al método "Save" del documento
// para modificar cómo ese método convierte el documento a PostScript.
// Establezca la propiedad "UseBookFoldPrintingSettings" a "true" para organizar el contenido
// en el documento Postscript de salida de manera que nos ayude a crear un folleto.
// Establezca la propiedad "UseBookFoldPrintingSettings" a "false" para guardar el documento normalmente.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::PsSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Ps);
saveOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Si estamos renderizando el documento como un folleto, debemos establecer la "MultiplePages"
// propiedades de los objetos de configuración de página de todas las secciones a "MultiplePagesType.BookFoldPrinting".
for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
{
    s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
}

// Una vez que imprimimos este documento en ambas caras de las páginas, podemos doblar todas las páginas por la mitad de una sola vez,
// y el contenido se alineará de manera que se forme un folleto.
doc->Save(get_ArtifactsDir() + u"PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
