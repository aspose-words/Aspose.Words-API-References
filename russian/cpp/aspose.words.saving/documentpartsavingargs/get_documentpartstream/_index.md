---
title: "метод Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream"
linktitle: "get_DocumentPartStream"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream. Позволяет указать поток, в который будет сохраняться часть документа в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartstream/
---
## DocumentPartSavingArgs::get_DocumentPartStream method


Позволяет указать поток, в который будет сохранена часть документа.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream() const
```

## Примечания


Это свойство позволяет сохранять части документа в потоки вместо файлов при экспорте в HTML.

Значение по умолчанию — **null**. Когда это свойство **null**, часть документа будет сохраняться в файл, указанный в свойстве [DocumentPartFileName](../get_documentpartfilename/).

Когда сохранение в поток в формате HTML запрашивается методами [Save()](../) или [Save()](../) и первая часть документа готовится к сохранению, Aspose.Words предлагает здесь основной выходной поток, первоначально переданный вызывающим.

При сохранении в формат EPUB, который является контейнерным форматом на основе HTML, [DocumentPartStream](./) не может быть указан, поскольку все вспомогательные части будут инкапсулированы в единый выходной пакет.

## См. также

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
