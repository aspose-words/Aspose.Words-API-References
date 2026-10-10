---
title: "Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts método"
linktitle: "get_GenerateFormFieldScripts"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts. Especifica si se deben generar scripts que emulan el comportamiento específico de los campos de formulario de Microsoft Word en PDF. El valor predeterminado es false en C++."
type: docs
weight: 18500
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_generateformfieldscripts/
---
## PdfSaveOptions::get_GenerateFormFieldScripts method


Especifica si se generan scripts que emulan el comportamiento específico de los campos de formulario de Microsoft Word en PDF. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts() const
```

## Observaciones


Cuando esta opción está habilitada, el exportador genera acciones de JavaScript en PDF para emular el comportamiento de los campos de formulario de Microsoft Word, como campos de fecha y hora con formato y reglas de validación.

Cuando se establece en **true**, el comportamiento compatible se exportará como acciones de JavaScript en PDF. Cuando se establece en **false**, no se generarán scripts de campos de formulario.

La ejecución de scripts depende del visor de PDF. Algunos visores de PDF pueden ignorar los scripts, restringir su ejecución o requerir que el usuario habilite JavaScript.

Las acciones de JavaScript están prohibidas por la conformidad PDF/A-1, PDF/A-2 y PDF/A-3. El valor **false** se utilizará automáticamente en este caso.
## Ver también

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
