---
title: "Aspose::Words::TabStop class"
linktitle: "TabStop"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TabStop class. Представляет одну пользовательскую табуляцию. Объект TabStop является членом коллекции TabStopCollection. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 68000
url: /ru/cpp/aspose.words/tabstop/
---
## TabStop class


Представляет одну пользовательскую табуляцию. Объект [TabStop](./) является членом коллекции [TabStopCollection](../tabstopcollection/). Чтобы узнать больше, посетите статью документации [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class TabStop : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Сравнивает с указанным [TabStop](./). |
| [get_Alignment](./get_alignment/)() const | Получает или задает выравнивание текста в этой табуляции. |
| [get_IsClear](./get_isclear/)() | Возвращает **true**, если эта табуляция удаляет любые существующие табуляции в этой позиции. |
| [get_Leader](./get_leader/)() const | Получает или задает тип линий‑заполнителей, отображаемых под символом табуляции. |
| [get_Position](./get_position/)() | Получает позицию табуляции в пунктах. |
| [GetHashCode](./gethashcode/)() const override | Вычисляет хеш-код для этого объекта. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::TabAlignment) | Сеттер для [Aspose::Words::TabStop::get_Alignment](./get_alignment/). |
| [set_Leader](./set_leader/)(Aspose::Words::TabLeader) | Сеттер для [Aspose::Words::TabStop::get_Leader](./get_leader/). |
| [TabStop](./tabstop/)(double) | Инициализирует новый экземпляр этого класса. |
| [TabStop](./tabstop/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Инициализирует новый экземпляр этого класса. |
| static [Type](./type/)() |  |
## Примечания


Обычно табуляция указывает позицию, где находится табуляция. Однако, поскольку табуляции могут наследоваться от стилей‑родителей, может потребоваться, чтобы дочерний объект явно указал отсутствие табуляции в заданной позиции. Чтобы удалить унаследованную табуляцию в определённой позиции, создайте объект [TabStop](./) и задайте [Alignment](./get_alignment/) значение [Clear](../tabalignment/).

Для получения дополнительной информации см. [TabStopCollection](../tabstopcollection/).

## Примеры



Показывает, как изменить позицию правой табуляции в абзацах, связанных с TOC.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table of contents.docx");

// Итерируйтесь по всем абзацам со стилями, основанными на результатах TOC; это любой стиль от TOC до TOC9.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    if (para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() >= Aspose::Words::StyleIdentifier::Toc1 && para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() <= Aspose::Words::StyleIdentifier::Toc9)
    {
        // Получите первую табуляцию, используемую в этом абзаце; она должна быть табуляцией, используемой для выравнивания номеров страниц.
        System::SharedPtr<Aspose::Words::TabStop> tab = para->get_ParagraphFormat()->get_TabStops()->idx_get(0);

        // Замените первую табуляцию по умолчанию пользовательской табуляцией.
        para->get_ParagraphFormat()->get_TabStops()->RemoveByPosition(tab->get_Position());
        para->get_ParagraphFormat()->get_TabStops()->Add(tab->get_Position() - 50, tab->get_Alignment(), tab->get_Leader());
    }
}

doc->Save(get_ArtifactsDir() + u"Styles.ChangeTocsTabStops.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
