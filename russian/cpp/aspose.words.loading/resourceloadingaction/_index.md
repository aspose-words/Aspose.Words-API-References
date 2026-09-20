---
title: "Aspose::Words::Loading::ResourceLoadingAction перечисление"
linktitle: "ResourceLoadingAction"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::ResourceLoadingAction перечисление. Указывает режим загрузки ресурсов. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words.loading/resourceloadingaction/
---
## ResourceLoadingAction enum


Указывает режим загрузки ресурсов. Чтобы узнать больше, посетите статью документации [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
enum class ResourceLoadingAction
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Default | 0 | Aspose.Words загрузит этот ресурс как обычно. |
| Пропустить | 1 | Aspose.Words пропустит загрузку этого ресурса. Для изображения будет сохранена только ссылка без данных, таблица стилей CSS будет игнорироваться в формате HTML. |
| UserProvided | 2 | Aspose.Words будет использовать массив байтов, предоставленный пользователем в [SetData()](../), в качестве данных ресурса. |

## См. также

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
