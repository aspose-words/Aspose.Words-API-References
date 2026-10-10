---
title: "Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings método"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings método. Obtiene o establece un valor booleano que indica si el documento debe guardarse usando un diseño de impresión en folleto, si está especificado mediante MultiplePages en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/pssaveoptions/get_usebookfoldprintingsettings/
---
## PsSaveOptions::get_UseBookFoldPrintingSettings method


Obtiene o establece un valor booleano que indica si el documento debe guardarse usando un diseño de impresión en folleto, si se especifica mediante [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/).

```cpp
bool Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Observaciones


Si se especifica esta opción, [PageSet](../../fixedpagesaveoptions/get_pageset/) se ignora al guardar. Este comportamiento coincide con MS Word. Si no se especifican los ajustes de impresión de plegado de libro en la configuración de página, esta opción no tendrá efecto.

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

* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
