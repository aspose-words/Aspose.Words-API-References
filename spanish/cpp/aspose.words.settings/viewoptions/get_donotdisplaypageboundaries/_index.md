---
title: "Método get_DoNotDisplayPageBoundaries de Aspose::Words::Settings::ViewOptions"
linktitle: "get_DoNotDisplayPageBoundaries"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_DoNotDisplayPageBoundaries de Aspose::Words::Settings::ViewOptions. Desactiva la visualización del espacio entre la parte superior del texto y el borde superior de la página en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.settings/viewoptions/get_donotdisplaypageboundaries/
---
## ViewOptions::get_DoNotDisplayPageBoundaries method


Desactiva la visualización del espacio entre la parte superior del texto y el borde superior de la página.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries() const
```


## Ejemplos



Muestra cómo ocultar el espacio vertical en blanco y los encabezados/pies de página en las opciones de vista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte contenido que abarque 3 páginas.
builder->Writeln(u"Paragraph 1, Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 2, Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 3, Page 3.");

// Inserte un encabezado y un pie de página.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the footer.");

// Este documento contiene una pequeña cantidad de contenido que ocupa el espacio equivalente a unas cuantas páginas completas.
// Establezca la bandera "DoNotDisplayPageBoundaries" a "true" para que las versiones anteriores de Microsoft Word omitan los encabezados,
// pies de página, y gran parte del espacio vertical en blanco al mostrar nuestro documento.
// Establezca la bandera "DoNotDisplayPageBoundaries" a "false" para que las versiones anteriores de Microsoft Word
// muestren normalmente nuestro documento.
doc->get_ViewOptions()->set_DoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayPageBoundaries.doc");
```

## Ver también

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
