---
title: "Метод Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri"
linktitle: "get_ResourceFileUri"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri. Получает или задает унифицированный идентификатор ресурса (URI), используемый для ссылки на файл ресурса из документа в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/resourcesavingargs/get_resourcefileuri/
---
## ResourceSavingArgs::get_ResourceFileUri method


Получает или задает унифицированный идентификатор ресурса (URI), используемый для ссылки на файл ресурса из документа.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri() const
```

## Примечания


Это свойство позволяет изменять URI файлов ресурсов, экспортируемых в фиксированный HTML, SVG или Markdown.

Aspose.Words автоматически генерирует URI для каждого файла ресурса при экспорте в фиксированный HTML, SVG и Markdown. Сгенерированные URI ссылаются на файлы ресурсов, сохранённые Aspose.Words. Однако URI могут быть некорректными, если файлы ресурсов перемещаются в другое место или сохраняются в потоки. Это свойство позволяет исправлять URI в таких случаях.

Когда событие вызывается, это свойство содержит URI, сгенерированный Aspose.Words. Вы можете изменить значение этого свойства, чтобы задать пользовательский URI для файла ресурса.
## См. также

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
