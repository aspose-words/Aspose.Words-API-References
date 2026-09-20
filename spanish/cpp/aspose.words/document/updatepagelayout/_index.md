---
title: "Aspose::Words::Document::UpdatePageLayout method"
linktitle: "UpdatePageLayout"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::UpdatePageLayout method. Reconstruye el diseño de página del documento en C++."
type: docs
weight: 98000
url: /es/cpp/aspose.words/document/updatepagelayout/
---
## Document::UpdatePageLayout method


Reconstruye el diseño de página del documento.

```cpp
void Aspose::Words::Document::UpdatePageLayout()
```

## Observaciones


Este método formatea un documento en páginas y actualiza los campos relacionados con el número de página en el documento, como PAGE, PAGES, PAGEREF y REF. La información actualizada del diseño de página es necesaria para una representación correcta del documento en formatos de página fija.

Este método se invoca automáticamente cuando conviertes un documento a PDF, XPS, imagen o lo imprimes por primera vez. Sin embargo, si modificas el documento después de renderizarlo y luego intentas renderizarlo nuevamente, Aspose.Words no actualizará el diseño de página automáticamente. En este caso deberías llamar a [UpdatePageLayout](./) antes de volver a renderizar.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
