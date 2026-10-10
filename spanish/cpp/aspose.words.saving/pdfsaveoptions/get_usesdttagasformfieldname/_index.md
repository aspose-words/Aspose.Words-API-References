---
title: "Método Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName"
linktitle: "get_UseSdtTagAsFormFieldName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName. Especifica si se debe usar la etiqueta Tag o la propiedad Id del control SDT como nombre del campo de formulario en PDF en C++."
type: docs
weight: 32500
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_usesdttagasformfieldname/
---
## PdfSaveOptions::get_UseSdtTagAsFormFieldName method


Especifica si se debe usar la etiqueta Tag o la propiedad Id del control SDT como nombre del campo de formulario en PDF.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName() const
```

## Observaciones


El valor predeterminado es **false**.

Cuando se establece en **false**, se usa la propiedad Id del control SDT como nombre del campo de formulario en PDF.

Cuando se establece en **true**, se usa la propiedad Tag del control SDT como nombre del campo de formulario en PDF.

Si se establece en **true** y Tag está vacío, se usará la propiedad Id como nombre del campo de formulario.

Si se establece en **true** y los valores de Tag no son únicos, los valores duplicados de Tag se modificarán para crear nombres únicos de campos de formulario PDF.
## Ver también

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
