---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources metodo"
linktitle: "get_ExportFontResources"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources. Specifica se le risorse dei caratteri devono essere esportate in HTML, MHTML o EPUB. Il valore predefinito è false in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontresources/
---
## HtmlSaveOptions::get_ExportFontResources method


Specifica se le risorse dei font devono essere esportate in HTML, MHTML o EPUB. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources() const
```

## Note


L'esportazione delle risorse dei caratteri consente una resa coerente del documento indipendente dai caratteri disponibili nell'ambiente di un utente.

Se [ExportFontResources](./) è impostato su **true**, il documento HTML principale farà riferimento a ogni carattere tramite la regola CSS 3 **%@font-face** e i caratteri saranno esportati come file separati. Quando si esporta nei formati IDPF EPUB o MHTML, i caratteri saranno incorporati nel relativo pacchetto insieme agli altri file secondari.

Se [ExportFontsAsBase64](../get_exportfontsasbase64/) è impostato su **true**, i caratteri non saranno salvati come file separati. Invece, saranno incorporati nelle regole **%@font-face** in codifica Base64.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
