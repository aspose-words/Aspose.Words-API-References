---
title: "Aspose::Words::Margins enum"
linktitle: "Márgenes"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Margins enum. Especifica márgenes predefinidos en C++."
type: docs
weight: 99000
url: /es/cpp/aspose.words/margins/
---
## Margins enum


Especifica los márgenes predefinidos.

```cpp
enum class Margins
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Normal | 0 | Márgenes normales. |
| Estrecho | 1 | Márgenes estrechos. |
| Moderado | 2 | Márgenes moderados. |
| Ancho | 3 | Márgenes anchos. |
| Espejado | 4 | Márgenes espejados. |
| Personalizado | 5 | Márgenes personalizados. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
