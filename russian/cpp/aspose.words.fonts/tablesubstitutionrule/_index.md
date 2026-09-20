---
title: "класс Aspose::Words::Fonts::TableSubstitutionRule"
linktitle: "TableSubstitutionRule"
second_title: "Справочник API Aspose.Words для C++"
description: "класс Aspose::Words::Fonts::TableSubstitutionRule. Правило замены шрифтов таблицы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 18000
url: /ru/cpp/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class


Табличное правило подстановки шрифтов. Чтобы узнать больше, посетите статью документации [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class TableSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Методы

| Метод | Описание |
| --- | --- |
| [AddSubstitutes](./addsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Добавляет альтернативные имена шрифтов для заданного оригинального имени шрифта. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Указывает, включено правило или нет. |
| [GetSubstitutes](./getsubstitutes/)(const System::String\&) | Возвращает массив, содержащий альтернативные имена шрифтов для указанного оригинального имени шрифта. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Load](./load/)(const System::String\&) | Загружает настройки замены таблицы из XML‑файла. |
| [Load](./load/)(const System::SharedPtr\<System::IO::Stream\>\&) | Загружает настройки замены таблицы из XML‑потока. |
| [LoadAndroidSettings](./loadandroidsettings/)() | Загружает предопределённые настройки замены таблицы для платформы Android. |
| [LoadLinuxSettings](./loadlinuxsettings/)() | Загружает предопределённые настройки замены таблицы для платформы Linux. |
| [LoadWindowsSettings](./loadwindowssettings/)() | Загружает предопределённые настройки замены таблицы для платформы Windows. |
| [Save](./save/)(const System::String\&) | Сохраняет текущие настройки замены таблицы в файл. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Сохраняет текущие настройки замены таблицы в поток. |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Сеттер для [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| [SetSubstitutes](./setsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Переопределяет имена заменяющих шрифтов для указанного оригинального имени шрифта. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как получить доступ к таблицам замены шрифтов для Windows и Linux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Создайте новое правило замены таблицы и загрузите таблицу замены шрифтов Microsoft Windows по умолчанию.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();
tableSubstitutionRule->LoadWindowsSettings();

// В Windows заменой по умолчанию для шрифта "Times New Roman CE" является "Times New Roman".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Times New Roman"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Мы можем сохранить таблицу в виде XML‑документа.
tableSubstitutionRule->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Windows.xml");

// У Linux есть собственная таблица замены.
// Для "Times New Roman CE" существует несколько заменяющих шрифтов.
// Если первая замена, "FreeSerif", также недоступна,
// это правило будет последовательно проверять остальные в массиве, пока не найдёт доступную.
tableSubstitutionRule->LoadLinuxSettings();
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"FreeSerif", u"Liberation Serif", u"DejaVu Serif"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Сохраните таблицу замены Linux в виде XML‑документа, используя поток.
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Linux.xml", System::IO::FileMode::Create);
    tableSubstitutionRule->Save(fileStream);
}
```

## См. также

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
