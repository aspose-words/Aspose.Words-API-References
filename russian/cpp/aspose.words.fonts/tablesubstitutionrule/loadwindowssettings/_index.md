---
title: "Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings метод"
linktitle: "LoadWindowsSettings"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings метод. Загружает предопределённые настройки замены таблиц для платформы Windows в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/
---
## TableSubstitutionRule::LoadWindowsSettings method


Загружает предопределённые настройки замены таблицы для платформы Windows.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings()
```


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

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
