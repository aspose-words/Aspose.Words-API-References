---
title: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow метод"
linktitle: "get_OpenHyperlinksInNewWindow"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow метод. Получает или задает значение, определяющее, принудительно ли открывать гиперссылки в выходном PDF‑документе в новом окне (или вкладке) браузера в C++."
type: docs
weight: 24000
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_openhyperlinksinnewwindow/
---
## PdfSaveOptions::get_OpenHyperlinksInNewWindow method


Получает или задаёт значение, определяющее, принудительно ли открывать гиперссылки в выходном Pdf‑документе в новом окне (или вкладке) браузера.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow() const
```

## Примечания


Значение по умолчанию — **false**. Когда это значение установлено в **true**, гиперссылки сохраняются с помощью JavaScript‑кода. JavaScript‑код выглядит как **app.launchURL("URL", true);**, где **URL** — гиперссылка.

Обратите внимание, что если эта опция установлена в **true**, гиперссылки могут не работать в некоторых PDF‑просмотрщиках, например Chrome, Firefox.

Действия JavaScript запрещены в соответствии с PDF/A-1, PDF/A-2 и PDF/A-3. Значение **false** будет использовано автоматически в этом случае.
## См. также

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
