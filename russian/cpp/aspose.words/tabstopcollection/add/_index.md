---
title: "Aspose::Words::TabStopCollection::Add method"
linktitle: "Add"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TabStopCollection::Add метод. Добавляет или заменяет табуляцию в коллекции в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/tabstopcollection/add/
---
## TabStopCollection::Add(const System::SharedPtr\<Aspose::Words::TabStop\>\&) method


Добавляет или заменяет табуляцию в коллекции.

```cpp
void Aspose::Words::TabStopCollection::Add(const System::SharedPtr<Aspose::Words::TabStop> &tabStop)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| tabStop | const System::SharedPtr\<Aspose::Words::TabStop\>\& | Объект табуляции для добавления. |
## Примечания


Если табуляция уже существует в указанной позиции, она будет заменена.

## Примеры



Показывает, как добавить пользовательские табуляции в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Ниже представлены два способа добавления табуляций в коллекцию табуляций абзаца через свойство "ParagraphFormat".
// 1 -  Создайте объект "TabStop", а затем добавьте его в коллекцию:
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Передайте значения свойств новой табуляции в метод "Add":
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Добавьте табуляции на 5 см ко всем абзацам.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// Каждый символ "tab" перемещает курсор построителя к позиции следующей табуляции.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## См. также

* Class [TabStop](../../tabstop/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## TabStopCollection::Add(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) method


Добавляет или заменяет табуляцию в коллекции.

```cpp
void Aspose::Words::TabStopCollection::Add(double position, Aspose::Words::TabAlignment alignment, Aspose::Words::TabLeader leader)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| позиция | double | Позиция (в пунктах), в которой следует добавить табуляцию. |
| alignment | Aspose::Words::TabAlignment | Значение [TabAlignment](../../tabalignment/) , которое определяет выравнивание текста у табуляции. |
| leader | Aspose::Words::TabLeader | Значение [TabLeader](../../tableader/) , которое определяет тип линий‑заполнителей, отображаемых под символом табуляции. |
## Примечания


Если табуляция уже существует в указанной позиции, она будет заменена.

## Примеры



Показывает, как добавить пользовательские табуляции в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Ниже представлены два способа добавления табуляций в коллекцию табуляций абзаца через свойство "ParagraphFormat".
// 1 -  Создайте объект "TabStop", а затем добавьте его в коллекцию:
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Передайте значения свойств новой табуляции в метод "Add":
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Добавьте табуляции на 5 см ко всем абзацам.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// Каждый символ "tab" перемещает курсор построителя к позиции следующей табуляции.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## См. также

* Enum [TabAlignment](../../tabalignment/)
* Enum [TabLeader](../../tableader/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
