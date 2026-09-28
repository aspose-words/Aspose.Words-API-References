---
title: "Класс Aspose::Words::TabStopCollection"
linktitle: "TabStopCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::TabStopCollection. Коллекция объектов TabStop, представляющих пользовательские табуляции для абзаца или стиля. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 69000
url: /ru/cpp/aspose.words/tabstopcollection/
---
## TabStopCollection class


Коллекция объектов [TabStop](../tabstop/), представляющих пользовательские табуляции для абзаца или стиля. Чтобы узнать больше, посетите статью документации [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class TabStopCollection : public Aspose::Words::InternableComplexAttr,
                          public Aspose::Words::IExpandableAttr
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Добавляет или заменяет табуляцию в коллекции. |
| [Add](./add/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Добавляет или заменяет табуляцию в коллекции. |
| [After](./after/)(double) | Получает первую табуляцию справа от указанной позиции. |
| [Before](./before/)(double) | Получает первую табуляцию слева от указанной позиции. |
| [Clear](./clear/)() | Удаляет все позиции табуляций. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStopCollection\>\&) | Определяет, равна ли указанная [TabStopCollection](./) по значению текущей [TabStopCollection](./). |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Определяет, равен ли указанный объект по значению текущему объекту. |
| [get_Count](./get_count/)() | Получает количество табуляций в коллекции. |
| [GetHashCode](./gethashcode/)() const override | Служит хеш-функцией для этого типа. |
| [GetIndexByPosition](./getindexbyposition/)(double) | Получает индекс табуляции с указанной позицией в пунктах. |
| [GetPositionByIndex](./getpositionbyindex/)(int32_t) | Получает позицию (в пунктах) табуляции по указанному индексу. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Получает табуляцию по заданному индексу. |
| [idx_get](./idx_get/)(double) | Получает табуляцию по указанной позиции. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveByIndex](./removebyindex/)(int32_t) | Удаляет табуляцию по указанному индексу из коллекции. |
| [RemoveByPosition](./removebyposition/)(double) | Удаляет табуляцию по указанной позиции из коллекции. |
| static [Type](./type/)() |  |
## Примечания


В документах Microsoft Word табуляцию можно задать в свойствах стиля абзаца или непосредственно в свойствах абзаца. Стиль может быть основан на другом стиле. Поэтому полный набор табуляций для данного объекта представляет собой комбинацию табуляций, определённых непосредственно для этого объекта, и табуляций, унаследованных от родительских стилей.

В Aspose.Words, когда вы получаете [TabStopCollection](./) для абзаца или стиля, она содержит только пользовательские табуляции, определённые непосредственно для этого абзаца или стиля. Коллекция не включает табуляции, определённые в родительских стилях, или табуляции по умолчанию.

## Примеры



Показывает, как работать с коллекцией табуляций документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = builder->get_ParagraphFormat()->get_TabStops();

// 72 пункта — это один «дюйм» на линейке табуляций Microsoft Word.
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(72.0));
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(432.0, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Dashes));

ASSERT_EQ(2, tabStops->get_Count());
ASSERT_FALSE(tabStops->idx_get(0)->get_IsClear());
ASSERT_FALSE(System::ObjectExt::Equals(tabStops->idx_get(0), tabStops->idx_get(1)));

// Каждый символ "tab" перемещает курсор построителя к позиции следующей табуляции.
builder->Writeln(u"Start\tTab 1\tTab 2");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(2, paragraphs->get_Count());

// Каждый абзац получает свою коллекцию табуляций, которая копирует значения из коллекции табуляций построителя документа.
ASPOSE_ASSERT_EQ(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());
ASPOSE_ASSERT_NS(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());

// Коллекция табуляций может указывать на TabStops до и после определённых позиций.
ASPOSE_ASSERT_EQ(72.0, tabStops->Before(100.0)->get_Position());
ASPOSE_ASSERT_EQ(432.0, tabStops->After(100.0)->get_Position());

// Мы можем очистить коллекцию табуляций абзаца, чтобы вернуть поведение табуляции по умолчанию.
paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->Clear();

ASSERT_EQ(0, paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.TabStopCollection.docx");
```

## См. также

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
