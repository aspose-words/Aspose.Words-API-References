---
title: "Aspose::Words::TabStopCollection::RemoveByPosition method"
linktitle: "RemoveByPosition"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TabStopCollection::RemoveByPosition метод. Удаляет табуляцию в указанной позиции из коллекции в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection::RemoveByPosition method


Удаляет табуляцию по указанной позиции из коллекции.

```cpp
void Aspose::Words::TabStopCollection::RemoveByPosition(double position)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| позиция | double | Позиция (в пунктах) табуляции, которую нужно удалить. |

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

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
