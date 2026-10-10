---
title: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow método"
linktitle: "get_OpenHyperlinksInNewWindow"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow método. Obtiene o establece un valor que determina si los hipervínculos en el documento Pdf de salida se forzan a abrirse en una nueva ventana (o pestaña) del navegador en C++."
type: docs
weight: 24000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_openhyperlinksinnewwindow/
---
## PdfSaveOptions::get_OpenHyperlinksInNewWindow method


Obtiene o establece un valor que determina si los hipervínculos en el documento Pdf de salida se forzan a abrirse en una nueva ventana (o pestaña) del navegador.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow() const
```

## Observaciones


El valor predeterminado es **false**. Cuando este valor se establece en **true**, los hipervínculos se guardan usando código JavaScript. El código JavaScript es **app.launchURL("URL", true);**, donde **URL** es un hipervínculo.

Tenga en cuenta que si esta opción se establece en **true**, los hipervínculos pueden no funcionar en algunos lectores de PDF, p. ej. Chrome, Firefox.

Las acciones de JavaScript están prohibidas por la conformidad PDF/A-1, PDF/A-2 y PDF/A-3. El valor **false** se utilizará automáticamente en este caso.
## Ver también

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
