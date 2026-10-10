---
title: "Método Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages"
linktitle: "get_PreblendImages"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages. Obtiene o establece un valor que determina si se deben premezclar imágenes transparentes con un color de fondo negro en C++."
type: docs
weight: 27000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_preblendimages/
---
## PdfSaveOptions::get_PreblendImages method


Obtiene o establece un valor que determina si se deben premezclar imágenes transparentes con color de fondo negro.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages() const
```

## Observaciones


Premezclar imágenes puede mejorar la apariencia visual del documento PDF en Adobe Reader y eliminar artefactos de antialiasing.

Para mostrar correctamente las imágenes premezcladas, la aplicación visor de PDF debe admitir la entrada /Matte en el diccionario de imágenes de máscara suave. Además, la premezcla de imágenes puede disminuir el rendimiento de renderizado del PDF.

El valor predeterminado es **false**.
## Ver también

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
