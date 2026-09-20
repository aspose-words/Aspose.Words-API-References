---
title: "Метод Aspose::Words::Style::get_StyleIdentifier"
linktitle: "get_StyleIdentifier"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Style::get_StyleIdentifier. Получает независимый от локали идентификатор стиля для встроенного стиля в C++."
type: docs
weight: 17000
url: /ru/cpp/aspose.words/style/get_styleidentifier/
---
## Style::get_StyleIdentifier method


Получает независимый от локали идентификатор стиля для встроенного стиля.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Style::get_StyleIdentifier() const
```

## Примечания


Для пользовательских (настраиваемых) стилей это свойство возвращает [User](../../styleidentifier/).

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

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
