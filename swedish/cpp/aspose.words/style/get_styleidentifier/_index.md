---
title: "Aspose::Words::Style::get_StyleIdentifier metod"
linktitle: "get_StyleIdentifier"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Style::get_StyleIdentifier metod. Hämtar den lokalt oberoende stilidentifieraren för en inbyggd stil i C++."
type: docs
weight: 17000
url: /sv/cpp/aspose.words/style/get_styleidentifier/
---
## Style::get_StyleIdentifier method


Hämtar den språkoberoende stilidentifieraren för en inbyggd stil.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Style::get_StyleIdentifier() const
```

## Anmärkningar


För användardefinierade (anpassade) stilar returnerar denna egenskap [User](../../styleidentifier/).

## Exempel



Visar hur man ändrar positionen för det högra tabbstoppet i TOC-relaterade stycken.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table of contents.docx");

// Iterera genom alla stycken med TOC-resultatbaserade stilar; detta är någon stil mellan TOC och TOC9.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    if (para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() >= Aspose::Words::StyleIdentifier::Toc1 && para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() <= Aspose::Words::StyleIdentifier::Toc9)
    {
        // Hämta den första tabben som används i detta stycke, den bör vara den tab som används för att justera sidnumren.
        System::SharedPtr<Aspose::Words::TabStop> tab = para->get_ParagraphFormat()->get_TabStops()->idx_get(0);

        // Ersätt det första standardtabbstoppet med ett anpassat tabbstopp.
        para->get_ParagraphFormat()->get_TabStops()->RemoveByPosition(tab->get_Position());
        para->get_ParagraphFormat()->get_TabStops()->Add(tab->get_Position() - 50, tab->get_Alignment(), tab->get_Leader());
    }
}

doc->Save(get_ArtifactsDir() + u"Styles.ChangeTocsTabStops.docx");
```

## Se även

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
