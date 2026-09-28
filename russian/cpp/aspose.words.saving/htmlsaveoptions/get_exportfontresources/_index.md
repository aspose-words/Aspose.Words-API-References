---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources метод"
linktitle: "get_ExportFontResources"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources. Указывает, следует ли экспортировать ресурсы шрифтов в HTML, MHTML или EPUB. По умолчанию значение false в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontresources/
---
## HtmlSaveOptions::get_ExportFontResources method


Указывает, следует ли экспортировать ресурсы шрифтов в HTML, MHTML или EPUB. По умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources() const
```

## Примечания


Экспорт ресурсов шрифтов обеспечивает согласованное отображение документа, независимо от шрифтов, доступных в среде конкретного пользователя.

Если [ExportFontResources](./) установлен в **true**, основной HTML‑документ будет ссылаться на каждый шрифт через правило CSS 3 **%@font-face**, а шрифты будут выводиться в виде отдельных файлов. При экспорте в форматы IDPF EPUB или MHTML шрифты будут внедрены в соответствующий пакет вместе с другими вспомогательными файлами.

Если [ExportFontsAsBase64](../get_exportfontsasbase64/) установлен в **true**, шрифты не будут сохраняться в отдельные файлы. Вместо этого они будут внедрены в правила **%@font-face** в кодировке Base64.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
