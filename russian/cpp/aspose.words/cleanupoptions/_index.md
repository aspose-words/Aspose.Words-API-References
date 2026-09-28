---
title: "Aspose::Words::CleanupOptions класс"
linktitle: "CleanupOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::CleanupOptions класс. Позволяет задавать параметры очистки документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/cleanupoptions/
---
## CleanupOptions class


Позволяет задавать параметры очистки документа. Чтобы узнать больше, посетите статью документации [Clean Up a Document](https://docs.aspose.com/words/cpp/clean-up-a-document/).

```cpp
class CleanupOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [CleanupOptions](./cleanupoptions/)() |  |
| [get_DuplicateStyle](./get_duplicatestyle/)() const | Получает/устанавливает флаг, указывающий, следует ли удалять дублирующие стили из документа. Значение по умолчанию — **false**. |
| [get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/)() const | Указывает, что неиспользуемые стили [BuiltIn](../style/get_builtin/) должны быть удалены из документа. |
| [get_UnusedLists](./get_unusedlists/)() const | Указывает, следует ли удалять из документа неиспользуемые списки и определения списков. Значение по умолчанию — **true**. |
| [get_UnusedStyles](./get_unusedstyles/)() const | Указывает, следует ли удалять из документа неиспользуемые стили. Значение по умолчанию — **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DuplicateStyle](./set_duplicatestyle/)(bool) | Сеттер для [Aspose::Words::CleanupOptions::get_DuplicateStyle](./get_duplicatestyle/). |
| [set_UnusedBuiltinStyles](./set_unusedbuiltinstyles/)(bool) | Сеттер для [Aspose::Words::CleanupOptions::get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/). |
| [set_UnusedLists](./set_unusedlists/)(bool) | Сеттер для [Aspose::Words::CleanupOptions::get_UnusedLists](./get_unusedlists/). |
| [set_UnusedStyles](./set_unusedstyles/)(bool) | Сеттер для [Aspose::Words::CleanupOptions::get_UnusedStyles](./get_unusedstyles/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как удалить все неиспользуемые пользовательские стили из документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// В сочетании со встроенными стилями документ теперь содержит восемь стилей.
// Пользовательский стиль помечается как "used", пока в документе есть любой текст
// отформатировано в этом стиле. Это означает, что 4 добавленных стиля в данный момент не используются.
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// Примените пользовательский символьный стиль, а затем пользовательский стиль списка. Это пометит их как "used".
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

// Сейчас есть один неиспользуемый символьный стиль и один неиспользуемый стиль списка.
// Метод Cleanup(), когда он настроен объектом CleanupOptions, может находить неиспользуемые стили и удалять их.
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_UnusedLists(true);
cleanupOptions->set_UnusedStyles(true);
cleanupOptions->set_UnusedBuiltinStyles(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Удаление каждого узла, к которому применён пользовательский стиль, снова помечает его как "unused".
// Повторно запустите метод Cleanup, чтобы удалить их.
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup(cleanupOptions);

ASSERT_EQ(2, doc->get_Styles()->get_Count());
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
