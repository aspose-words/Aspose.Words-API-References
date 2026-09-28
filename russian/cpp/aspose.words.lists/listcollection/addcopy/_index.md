---
title: "Aspose::Words::Lists::ListCollection::AddCopy метод"
linktitle: "AddCopy"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Lists::ListCollection::AddCopy метод. Создает новый список, копируя указанный список и добавляя его в коллекцию списков в документе в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.lists/listcollection/addcopy/
---
## ListCollection::AddCopy method


Создаёт новый список, копируя указанный список, и добавляет его в коллекцию списков в документе.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddCopy(const System::SharedPtr<Aspose::Words::Lists::List> &srcList)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| srcList | const System::SharedPtr\<Aspose::Words::Lists::List\>\& | Исходный список для копирования. |

### ReturnValue

Новосозданный список.
## Примечания


Исходный список может быть из любого документа. Если исходный список принадлежит другому документу, создается копия списка и добавляется в текущий документ.

Если исходный список является ссылкой на стиль списка или его определением, новосозданный список не связан с оригинальным стилем списка.

## Примеры



Показывает, как перезапустить нумерацию в списке, скопировав список.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Список позволяет организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
// Мы можем создавать вложенные списки, увеличивая уровень отступа.
// Мы можем начинать и завершать список, используя свойство "ListFormat" объекта document builder.
// Каждый абзац, который мы добавляем между началом и концом списка, становится элементом списка.
// Создайте список из шаблона Microsoft Word и настройте его первый уровень списка.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// Примените наш список к некоторым абзацам.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Мы можем добавить копию существующего списка в коллекцию списков документа
// чтобы создать похожий список без изменения оригинала.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// Примените второй список к новым абзацам.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## См. также

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
