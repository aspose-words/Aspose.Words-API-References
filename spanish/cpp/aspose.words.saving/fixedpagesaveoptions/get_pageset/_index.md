---
title: "Método Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet"
linktitle: "get_PageSet"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet. Obtiene o establece las páginas a renderizar. El valor predeterminado son todas las páginas del documento en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.saving/fixedpagesaveoptions/get_pageset/
---
## FixedPageSaveOptions::get_PageSet method


Obtiene o establece las páginas a renderizar. El valor predeterminado son todas las páginas del documento.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet() const
```


## Ejemplos



Muestra cómo extraer páginas basándose en índices de página exactos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agrega cinco páginas al documento.
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Crea un objeto "XpsSaveOptions", que podemos pasar al método "Save" del documento
// para modificar cómo ese método convierte el documento a .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// Utiliza la propiedad "PageSet" para seleccionar un conjunto de páginas del documento que se guardarán en la salida XPS.
// En este caso, elegiremos, mediante un índice basado en cero, solo tres páginas: página 1, página 2 y página 4.
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## Ver también

* Class [PageSet](../../pageset/)
* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
