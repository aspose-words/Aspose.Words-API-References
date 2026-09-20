---
title: "метод Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream"
linktitle: "get_ResourceStream"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream. Позволяет указать поток, в который будет сохраняться ресурс, в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.saving/resourcesavingargs/get_resourcestream/
---
## ResourceSavingArgs::get_ResourceStream method


Позволяет указать поток, в который будет сохранён ресурс.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream() const
```

## Примечания


Это свойство позволяет сохранять ресурсы в потоки вместо файлов.

Значение по умолчанию — **null**. Когда это свойство равно **null**, ресурс будет сохранён в файл, указанный в свойстве [ResourceFileName](../get_resourcefilename/).

Используя [IResourceSavingCallback](../../iresourcesavingcallback/), вы не можете заменить один ресурс другим. Это предназначено только для контроля над местом сохранения ресурсов.

## См. также

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
