---
title: "Класс Aspose::Words::Saving::DocumentPartSavingArgs"
linktitle: "DocumentPartSavingArgs"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Saving::DocumentPartSavingArgs. Предоставляет данные для обратного вызова DocumentPartSaving(). Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class


Предоставляет данные для обратного вызова [DocumentPartSaving()](../idocumentpartsavingcallback/documentpartsaving/). Чтобы узнать больше, посетите статью документации [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class DocumentPartSavingArgs : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Document](./get_document/)() const | Получает объект документа, который сохраняется. |
| [get_DocumentPartFileName](./get_documentpartfilename/)() const | Получает или задает имя файла (без пути), в который будет сохранена часть документа. |
| [get_DocumentPartStream](./get_documentpartstream/)() const | Позволяет указать поток, в который будет сохранена часть документа. |
| [get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/)() const | Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения части документа. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DocumentPartFileName](./set_documentpartfilename/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName](./get_documentpartfilename/). |
| [set_DocumentPartStream](./set_documentpartstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Сеттер для [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream](./get_documentpartstream/). |
| [set_DocumentPartStream](./set_documentpartstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepDocumentPartStreamOpen](./set_keepdocumentpartstreamopen/)(bool) | Сеттер для [Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/). |
| static [Type](./type/)() |  |
## Примечания


Когда Aspose.Words сохраняет документ в HTML или связанные форматы и указано [DocumentSplitCriteria](../htmlsaveoptions/get_documentsplitcriteria/), документ разбивается на части, и по умолчанию каждая часть документа сохраняется в отдельный файл.

Класс [DocumentPartSavingArgs](./) позволяет управлять тем, как будет сохраняться каждая часть документа. Он позволяет переопределить способ генерации имён файлов или полностью обойти сохранение частей документа в файлы, предоставив свои собственные объекты потоков.

Чтобы сохранять части документа в потоки вместо файлов, используйте свойство [DocumentPartStream](./get_documentpartstream/).
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
