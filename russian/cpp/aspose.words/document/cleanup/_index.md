---
title: "Aspose::Words::Document::Cleanup метод"
linktitle: "Cleanup"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::Cleanup. Очищает неиспользуемые стили и списки из документа в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/document/cleanup/
---
## Document::Cleanup() method


Очищает документ от неиспользуемых стилей и списков.

```cpp
void Aspose::Words::Document::Cleanup()
```


## Примеры



Показывает, как удалить неиспользуемые пользовательские стили из документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// В сочетании со встроенными стилями документ теперь содержит восемь стилей.
// Пользовательский стиль считается «использованным», когда применён к какой‑либо части документа,
// что означает, что четыре добавленных стиля в данный момент не используются.
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// Примените пользовательский символьный стиль, а затем пользовательский стиль списка. Это пометит стили как «использованные».
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Cleanup();

ASSERT_EQ(6, doc->get_Styles()->get_Count());

// Удаление каждого узла, к которому применён пользовательский стиль, снова помечает его как "unused".
// Запустите метод Cleanup ещё раз, чтобы удалить их.
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup();

ASSERT_EQ(4, doc->get_Styles()->get_Count());
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Cleanup(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) method


Очищает неиспользуемые стили и списки из документа в зависимости от указанных [CleanupOptions](../../cleanupoptions/).

```cpp
void Aspose::Words::Document::Cleanup(const System::SharedPtr<Aspose::Words::CleanupOptions> &options)
```


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

* Class [CleanupOptions](../../cleanupoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
