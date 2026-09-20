---
title: "Método Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields"
linktitle: "get_PreserveFormFields"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields. Especifica si se deben conservar los campos de formulario de Microsoft Word como campos de formulario en PDF o convertirlos a texto. El valor predeterminado es false en C++."
type: docs
weight: 28000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_preserveformfields/
---
## PdfSaveOptions::get_PreserveFormFields method


Especifica si se deben conservar los campos de formulario de Microsoft Word como campos de formulario en PDF o convertirlos a texto. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields() const
```

## Observaciones


Los campos de formulario de Microsoft Word incluyen controles de entrada de texto, listas desplegables y casillas de verificación.

Cuando se establece en **false**, estos campos se exportarán como texto a PDF. Cuando se establece en **true**, estos campos se exportarán como campos de formulario PDF.

Al exportar campos de formulario a PDF como campos de formulario, puede producirse cierta pérdida de formato porque los campos de formulario PDF no admiten todas las características de los campos de formulario de Microsoft Word.

Además, el tamaño de salida depende del tamaño del contenido porque los formularios editables en Microsoft Word son objetos en línea.
## Ver también

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
