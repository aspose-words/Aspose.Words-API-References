---
title: "Aspose::Words::Document::UpdateListLabels method"
linktitle: "UpdateListLabels"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::UpdateListLabels method. Uppdaterar listetiketter för alla listobjekt i dokumentet i C++."
type: docs
weight: 97000
url: /sv/cpp/aspose.words/document/updatelistlabels/
---
## Document::UpdateListLabels method


Uppdaterar listetiketter för alla listobjekt i dokumentet.

```cpp
void Aspose::Words::Document::UpdateListLabels()
```

## Anmärkningar


Denna metod uppdaterar listetikett‑egenskaper såsom [LabelValue](../../../aspose.words.lists/listlabel/get_labelvalue/) och [LabelString](../../../aspose.words.lists/listlabel/get_labelstring/) för varje [ListLabel](../../paragraph/get_listlabel/)‑objekt i dokumentet.

Dessutom anropas denna metod ibland implicit när fält i dokumentet uppdateras. Detta krävs eftersom vissa fält som kan referera till listnummer (t.ex. TOC eller REF) måste vara aktuella.

## Exempel



Visar hur man extraherar listetiketterna för alla stycken som är listobjekt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

// Hitta om vi har styckelistan. I vårt dokument använder vår lista vanliga arabiska siffror,
// som börjar på tre och slutar på sex.
for (auto&& paragraph : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"List item paragraph #{0}", paras->IndexOf(paragraph)) << std::endl;

    // Detta är texten vi får när vi hämtar och skriver ut den här noden i textformat.
    // Denna textutmatning kommer att utelämna listetiketter. Trimma eventuella tecken för styckeformatering.
    System::String paragraphText = paragraph->ToString(Aspose::Words::SaveFormat::Text).Trim();
    std::cout << System::String::Format(u"\tExported Text: {0}", paragraphText) << std::endl;

    System::SharedPtr<Aspose::Words::Lists::ListLabel> label = paragraph->get_ListLabel();

    // Detta hämtar positionen för stycket i den aktuella nivån i listan. Om vi har en lista med flera nivåer,
    // detta kommer att berätta vilken position det har på den nivån.
    std::cout << System::String::Format(u"\tNumerical Id: {0}", label->get_LabelValue()) << std::endl;

    // Kombinera dem tillsammans för att inkludera listetiketten med texten i utdata.
    std::cout << System::String::Format(u"\tList label combined with text: {0} {1}", label->get_LabelString(), paragraphText) << std::endl;
}
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
