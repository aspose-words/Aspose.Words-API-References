---
title: "Aspose::Words::Saving::ImlRenderingMode enum"
linktitle: "ImlRenderingMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImlRenderingMode enum. Especifica cómo se renderizan los objetos de tinta (InkML) a formatos de página fija en C++."
type: docs
weight: 66000
url: /es/cpp/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enum


Especifica cómo se renderizan los objetos de tinta (InkML) a formatos de página fija.

```cpp
enum class ImlRenderingMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Fallback | 0 | Si hay una forma de respaldo disponible para el objeto de tinta (InkML), Aspose.Words renderiza la forma de respaldo en lugar del InkML. |
| InkML | 1 | Aspose.Words ignora la forma de respaldo del objeto de tinta (InkML) y renderiza InkML directamente. Este es el modo predeterminado. |


## Ejemplos



Muestra cómo renderizar el objeto Ink.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Ink object.docx");

// Establezca 'ImlRenderingMode.InkML' para que ignore la forma de respaldo del objeto de tinta (InkML) y renderice InkML directamente.
// Si el resultado del renderizado es insatisfactorio,
// por favor use 'ImlRenderingMode.Fallback' para obtener un resultado similar a versiones anteriores.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
saveOptions->set_ImlRenderingMode(Aspose::Words::Saving::ImlRenderingMode::InkML);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
