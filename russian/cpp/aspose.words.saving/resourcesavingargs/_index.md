---
title: "Aspose::Words::Saving::ResourceSavingArgs class"
linktitle: "ResourceSavingArgs"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ResourceSavingArgs class. Предоставляет данные для события ResourceSaving(). Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 27000
url: /ru/cpp/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class


Предоставляет данные для события [ResourceSaving()](../iresourcesavingcallback/resourcesaving/). Чтобы узнать больше, посетите статью документации [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class ResourceSavingArgs : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Document](./get_document/)() const | Получает объект документа, который в данный момент сохраняется. |
| [get_KeepResourceStreamOpen](./get_keepresourcestreamopen/)() const | Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения ресурса. |
| [get_ResourceFileName](./get_resourcefilename/)() const | Получает или задает имя файла (без пути), в который будет сохранён ресурс. |
| [get_ResourceFileUri](./get_resourcefileuri/)() const | Получает или задает унифицированный идентификатор ресурса (URI), используемый для ссылки на файл ресурса из документа. |
| [get_ResourceStream](./get_resourcestream/)() const | Позволяет указать поток, в который будет сохранён ресурс. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_KeepResourceStreamOpen](./set_keepresourcestreamopen/)(bool) | Сеттер для [Aspose::Words::Saving::ResourceSavingArgs::get_KeepResourceStreamOpen](./get_keepresourcestreamopen/). |
| [set_ResourceFileName](./set_resourcefilename/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName](./get_resourcefilename/). |
| [set_ResourceFileUri](./set_resourcefileuri/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri](./get_resourcefileuri/). |
| [set_ResourceStream](./set_resourcestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Сеттер для [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream](./get_resourcestream/). |
| [set_ResourceStream](./set_resourcestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## Примечания


По умолчанию, когда Aspose.Words сохраняет документ в фиксированный HTML‑страницу, SVG или Markdown, каждый ресурс сохраняется в отдельный файл. Aspose.Words использует имя файла документа и уникальный номер для генерации уникального имени файла для каждого ресурса, найденного в документе.

[ResourceSavingArgs](./) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

Чтобы применить собственную логику генерации имён файлов ресурсов, используйте свойство [ResourceFileName](./get_resourcefilename/).

Чтобы сохранять ресурсы в потоки вместо файлов, используйте свойство [ResourceStream](./get_resourcestream/).
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
