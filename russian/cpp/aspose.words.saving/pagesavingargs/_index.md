---
title: "Класс Aspose::Words::Saving::PageSavingArgs"
linktitle: "PageSavingArgs"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Saving::PageSavingArgs. Предоставляет данные для события PageSaving(). Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class


Предоставляет данные для события [PageSaving()](../ipagesavingcallback/pagesaving/). Чтобы узнать больше, посетите статью документации [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageSavingArgs : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_KeepPageStreamOpen](./get_keeppagestreamopen/)() const | Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения страницы документа. |
| [get_PageFileName](./get_pagefilename/)() const | Получает имя файла, в который будет сохранена страница документа. |
| [get_PageIndex](./get_pageindex/)() const | Текущий индекс страницы. |
| [get_PageStream](./get_pagestream/)() const | Позволяет указать поток, в который будет сохранена страница документа. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSavingArgs](./pagesavingargs/)() |  |
| [set_KeepPageStreamOpen](./set_keeppagestreamopen/)(bool) | Сеттер для [Aspose::Words::Saving::PageSavingArgs::get_KeepPageStreamOpen](./get_keeppagestreamopen/). |
| [set_PageFileName](./set_pagefilename/)(const System::String\&) | Устанавливает имя файла, в который будет сохранена страница документа. |
| [set_PageStream](./set_pagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Сеттер для [Aspose::Words::Saving::PageSavingArgs::get_PageStream](./get_pagestream/). |
| [set_PageStream](./set_pagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
