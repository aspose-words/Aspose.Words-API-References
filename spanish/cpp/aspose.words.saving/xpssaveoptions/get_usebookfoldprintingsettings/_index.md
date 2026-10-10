---
title: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings método"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings método. Obtiene o establece un valor booleano que indica si el documento debe guardarse usando un diseño de impresión en folleto, si se especifica mediante MultiplePages en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/xpssaveoptions/get_usebookfoldprintingsettings/
---
## XpsSaveOptions::get_UseBookFoldPrintingSettings method


Obtiene o establece un valor booleano que indica si el documento debe guardarse usando un diseño de impresión en folleto, si se especifica mediante [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/).

```cpp
bool Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Observaciones


Si se especifica esta opción, [PageSet](../../fixedpagesaveoptions/get_pageset/) se ignora al guardar. Este comportamiento coincide con MS Word. Si no se especifican los ajustes de impresión de plegado de libro en la configuración de página, esta opción no tendrá efecto.

## Ejemplos



Muestra cómo guardar un documento en formato XPS en forma de pliegue de libro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Cree un objeto "XpsSaveOptions" que podamos pasar al método "Save" del documento
// para modificar cómo ese método convierte el documento a .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>(Aspose::Words::SaveFormat::Xps);

// Establezca la propiedad "UseBookFoldPrintingSettings" a "true" para organizar el contenido
// en el XPS de salida de manera que nos ayude a usarlo para crear un folleto.
// Establezca la propiedad "UseBookFoldPrintingSettings" a "false" para renderizar el XPS normalmente.
xpsOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Si estamos renderizando el documento como un folleto, debemos establecer la "MultiplePages"
// propiedades de los objetos de configuración de página de todas las secciones a "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
{
    for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
    }
}

// Una vez que imprimamos este documento, podemos convertirlo en un folleto apilando las páginas
// para salir de la impresora y plegarse por la mitad.
doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.BookFold.xps", xpsOptions);
```

## Ver también

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
