---
title: "Aspose::Words::Loading::ResourceLoadingArgs класс"
linktitle: "ResourceLoadingArgs"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::ResourceLoadingArgs класс. Предоставляет данные для метода ResourceLoading() в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class


Предоставляет данные для метода [ResourceLoading()](../iresourceloadingcallback/resourceloading/).

```cpp
class ResourceLoadingArgs : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_OriginalUri](./get_originaluri/)() const | Исходный URI ресурса, указанный в импортированном документе. |
| [get_ResourceType](./get_resourcetype/)() const | Тип ресурса. |
| [get_Uri](./get_uri/)() const | URI ресурса, используемый для загрузки, если [ResourceLoading()](../iresourceloadingcallback/resourceloading/) возвращает [Default](../resourceloadingaction/). Изначально он установлен в абсолютный URI ресурса, но пользователь может переопределить его на любое значение. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Uri](./set_uri/)(const System::String\&) | Сеттер для [Aspose::Words::Loading::ResourceLoadingArgs::get_Uri](./get_uri/). |
| [SetData](./setdata/)(const System::ArrayPtr\<uint8_t\>\&) | Устанавливает пользовательские данные ресурса, которые используются, если [ResourceLoading()](../iresourceloadingcallback/resourceloading/) возвращает [UserProvided](../resourceloadingaction/). |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
