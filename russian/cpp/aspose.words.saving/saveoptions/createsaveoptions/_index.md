---
title: "Метод Aspose::Words::Saving::SaveOptions::CreateSaveOptions"
linktitle: "CreateSaveOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::SaveOptions::CreateSaveOptions. Создает объект параметров сохранения класса, подходящего для указанного формата сохранения в C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.saving/saveoptions/createsaveoptions/
---
## SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat) method


Создаёт объект параметров сохранения класса, подходящего для указанного формата сохранения.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения, для которого необходимо создать объект параметров сохранения. |

### ReturnValue

Объект класса, наследующегося от [SaveOptions](../).

## См. также

* Class [SaveOptions](../)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## SaveOptions::CreateSaveOptions(const System::String\&) method


Создаёт объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(const System::String &fileName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Расширение этого имени файла определяет класс создаваемого объекта параметров сохранения. |

### ReturnValue

Объект класса, наследующегося от [SaveOptions](../).

## Примеры



Показывает, как установить шаблон по умолчанию для документов, у которых нет прикреплённых шаблонов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Включите автоматическое обновление стилей, но не прикрепляйте документ шаблона.
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Поскольку шаблонного документа нет, у документа не было места для отслеживания изменений стилей.
// Используйте объект SaveOptions, чтобы автоматически установить шаблон
// если документ, который мы сохраняем, не имеет его.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(get_MyDir() + u"Business brochure.dotx");

doc->Save(get_ArtifactsDir() + u"Document.DefaultTemplate.docx", options);
```

## См. также

* Class [SaveOptions](../)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
