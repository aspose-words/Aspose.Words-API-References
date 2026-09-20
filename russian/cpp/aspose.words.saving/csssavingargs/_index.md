---
title: "Aspose::Words::Saving::CssSavingArgs класс"
linktitle: "CssSavingArgs"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::CssSavingArgs класс. Предоставляет данные для события CssSaving(). Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class


Предоставляет данные для события [CssSaving()](../icsssavingcallback/csssaving/). Чтобы узнать больше, посетите статью документации [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class CssSavingArgs : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_CssStream](./get_cssstream/)() const | Позволяет указать поток, в который будет сохраняться информация CSS. |
| [get_Document](./get_document/)() const | Получает объект документа, который в данный момент сохраняется. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Позволяет указать, будет ли CSS экспортироваться в файл и встраиваться в HTML‑документ. По умолчанию **true**. Когда это свойство **false**, информация CSS не будет сохраняться в файл CSS и не будет встраиваться в HTML‑документ. |
| [get_KeepCssStreamOpen](./get_keepcssstreamopen/)() const | Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения информации CSS. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CssStream](./set_cssstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Сеттер для [Aspose::Words::Saving::CssSavingArgs::get_CssStream](./get_cssstream/). |
| [set_CssStream](./set_cssstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Позволяет указать, будет ли CSS экспортироваться в файл и встраиваться в HTML‑документ. По умолчанию **true**. Когда это свойство **false**, информация CSS не будет сохраняться в файл CSS и не будет встраиваться в HTML‑документ. |
| [set_KeepCssStreamOpen](./set_keepcssstreamopen/)(bool) | Сеттер для [Aspose::Words::Saving::CssSavingArgs::get_KeepCssStreamOpen](./get_keepcssstreamopen/). |
| static [Type](./type/)() |  |
## Примечания


По умолчанию, когда Aspose.Words сохраняет документ в HTML, он сохраняет информацию CSS встроенно (в виде значения атрибута **style** у каждого элемента).

[CssSavingArgs](./) allows to save CSS information into file by providing your own stream object.

Чтобы сохранить CSS в поток, используйте свойство [CssStream](./get_cssstream/).

Чтобы отключить сохранение CSS в файл и встраивание в HTML‑документ, используйте свойство [IsExportNeeded](./get_isexportneeded/).
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
