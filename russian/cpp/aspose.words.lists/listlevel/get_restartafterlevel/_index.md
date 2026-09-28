---
title: "Aspose::Words::Lists::ListLevel::get_RestartAfterLevel метод"
linktitle: "get_RestartAfterLevel"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Lists::ListLevel::get_RestartAfterLevel метод. Устанавливает или возвращает уровень списка, который должен появиться перед тем, как указанный уровень списка перезапускает нумерацию в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.lists/listlevel/get_restartafterlevel/
---
## ListLevel::get_RestartAfterLevel method


Задает или возвращает уровень списка, который должен предшествовать указанному уровню списка, перезапускающему нумерацию.

```cpp
int32_t Aspose::Words::Lists::ListLevel::get_RestartAfterLevel() const
```

## Примечания


Значение -1 означает, что нумерация будет продолжаться.

## Примеры



Показывает продвинутые способы настройки меток списка.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Список позволяет организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
// Мы можем создавать вложенные списки, увеличивая уровень отступа.
// Мы можем начинать и завершать список, используя свойство "ListFormat" объекта document builder.
// Каждый абзац, который мы добавляем между началом и концом списка, становится элементом списка.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

// Метк� уровня 1 будут отформатированы в соответствии со стилем абзаца "Heading 1" и будут иметь префикс.
// Они будут выглядеть как "Appendix A", "Appendix B"...
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"Appendix \x0000");
list->get_ListLevels()->idx_get(0)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);
list->get_ListLevels()->idx_get(0)->set_LinkedStyle(doc->get_Styles()->idx_get(u"Heading 1"));

// Метк� уровня 2 будут отображать текущие номера первого и второго уровней списка и иметь ведущие нули.
// Если первый уровень списка равен 1, то метки списка будут выглядеть как "Section (1.01)", "Section (1.02)"...
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"Section (\x0000" u".\x0001" u")");
list->get_ListLevels()->idx_get(1)->set_NumberStyle(Aspose::Words::NumberStyle::LeadingZero);

// Обратите внимание, что более высокий уровень использует нумерацию UppercaseLetter.
// Мы можем установить свойство "IsLegal", чтобы использовать арабские цифры для более высоких уровней списка.
list->get_ListLevels()->idx_get(1)->set_IsLegal(true);
list->get_ListLevels()->idx_get(1)->set_RestartAfterLevel(0);

// Метк� уровня 3 будут представлять собой заглавные римские цифры с префиксом и суффиксом и будут перезапускаться для каждого элемента уровня 1 списка.
// Эти метки списка будут выглядеть как "-I-", "-II-"...
list->get_ListLevels()->idx_get(2)->set_NumberFormat(u"-\x0002" u"-");
list->get_ListLevels()->idx_get(2)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
list->get_ListLevels()->idx_get(2)->set_RestartAfterLevel(1);

// Сделайте метки всех уровней списка полужирными.
for (auto&& level : list->get_ListLevels())
{
    level->get_Font()->set_Bold(true);
}

// Примените форматирование списка к текущему абзацу.
builder->get_ListFormat()->set_List(list);

// Создайте элементы списка, которые будут отображать все три наших уровня списка.
for (int32_t n = 0; n < 2; n++)
{
    for (int32_t i = 0; i < 3; i++)
    {
        builder->get_ListFormat()->set_ListLevelNumber(i);
        builder->Writeln(System::String(u"Level ") + i);
    }
}

builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.CreateListRestartAfterHigher.docx");
```

## См. также

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
