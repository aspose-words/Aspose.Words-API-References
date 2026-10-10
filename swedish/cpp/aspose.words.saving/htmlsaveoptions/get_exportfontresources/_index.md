---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources metod"
linktitle: "get_ExportFontResources"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources metod. Anger om teckensnittresurser ska exporteras till HTML, MHTML eller EPUB. Standard är falskt i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontresources/
---
## HtmlSaveOptions::get_ExportFontResources method


Anger om teckensnittresurser ska exporteras till HTML, MHTML eller EPUB. Standard är **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources() const
```

## Anmärkningar


Export av teckensnittresurser möjliggör konsekvent dokumentrendering oberoende av de teckensnitt som finns i en viss användares miljö.

Om [ExportFontResources](./) är inställd på **true**, kommer huvud‑HTML‑dokumentet att referera till varje teckensnitt via CSS 3‑regeln **%@font-face** och teckensnitten kommer att skrivas ut som separata filer. Vid export till IDPF EPUB‑ eller MHTML‑format kommer teckensnitten att bäddas in i motsvarande paket tillsammans med andra underordnade filer.

Om [ExportFontsAsBase64](../get_exportfontsasbase64/) är inställd på **true**, kommer teckensnitt inte att sparas som separata filer. Istället kommer de att bäddas in i **%@font-face**‑regler i Base64‑kodning.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
