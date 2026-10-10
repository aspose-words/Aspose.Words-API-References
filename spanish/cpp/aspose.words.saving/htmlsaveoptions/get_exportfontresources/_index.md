---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources método"
linktitle: "get_ExportFontResources"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources. Especifica si los recursos de fuentes deben exportarse a HTML, MHTML o EPUB. El valor predeterminado es false en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontresources/
---
## HtmlSaveOptions::get_ExportFontResources method


Especifica si los recursos de fuentes deben exportarse a HTML, MHTML o EPUB. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources() const
```

## Observaciones


Exportar recursos de fuentes permite una renderización de documentos consistente, independiente de las fuentes disponibles en el entorno de un usuario determinado.

Si [ExportFontResources](./) está configurado en **true**, el documento HTML principal hará referencia a cada fuente mediante la regla at‑rule CSS 3 **%@font-face** y las fuentes se exportarán como archivos separados. Al exportar a los formatos IDPF EPUB o MHTML, las fuentes se incrustarán en el paquete correspondiente junto con otros archivos auxiliares.

Si [ExportFontsAsBase64](../get_exportfontsasbase64/) está configurado en **true**, las fuentes no se guardarán en archivos separados. En su lugar, se incrustarán en las reglas at‑rule **%@font-face** con codificación Base64.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
