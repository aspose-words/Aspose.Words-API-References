---
title: "Método Aspose::Words::PageSetup::get_Margins"
linktitle: "get_Margins"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::PageSetup::get_Margins. Devuelve o establece los Márgenes predefinidos de la página en C++."
type: docs
weight: 28000
url: /es/cpp/aspose.words/pagesetup/get_margins/
---
## PageSetup::get_Margins method


Devuelve o establece los [Margins](../../margins/) predefinidos de la página.

```cpp
Aspose::Words::Margins Aspose::Words::PageSetup::get_Margins()
```


## Ejemplos



Muestra cuándo recalcular el diseño de página del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Guardar un documento en PDF, en una imagen o imprimirlo por primera vez lo hará automáticamente
// almacenar en caché el diseño del documento dentro de sus páginas.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Modifique el documento de alguna manera.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// En la versión actual de Aspose.Words, modificar el documento no vuelve a reconstruir automáticamente
// el diseño de página en caché. Si deseamos que el diseño en caché
// se mantenga actualizado, necesitaremos actualizarlo manualmente.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## Ver también

* Enum [Margins](../../margins/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
