---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName method"
linktitle: "get_CssStyleSheetFileName"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName method. Указывает путь и имя файла каскадных таблиц стилей (CSS), записываемого при экспорте документа в HTML. По умолчанию пустая строка в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheetfilename/
---
## HtmlSaveOptions::get_CssStyleSheetFileName method


Указывает путь и имя каскадного [Style](../../../aspose.words/style/) листа (CSS), записываемого при экспорте документа в HTML. По умолчанию пустая строка.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName() const
```

## Примечания


Это свойство действует только при сохранении документа в формате HTML и когда внешний CSS‑лист запрашивается с помощью [CssStyleSheetType](../get_cssstylesheettype/).

Если это свойство пусто, файл CSS будет сохранён в той же папке и с тем же именем, что и HTML‑документ, но с расширением ".css".

Если в этом свойстве указан только путь без имени файла, файл CSS будет сохранён в указанной папке и получит то же имя, что и HTML‑документ, но с расширением ".css".

Если папка, указанная в этом свойстве, не существует, она будет создана автоматически перед сохранением файла CSS.

Другой способ указать папку для сохранения внешнего файла CSS — использовать [ResourceFolder](../get_resourcefolder/).

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
