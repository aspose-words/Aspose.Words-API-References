---
title: "Aspose::Words::TabStop-klass"
linktitle: "TabStop"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TabStop klass. Representerar ett enda anpassat tabbstopp. TabStop-objektet är en medlem av TabStopCollection-samlingen. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 68000
url: /sv/cpp/aspose.words/tabstop/
---
## TabStop class


Representerar ett enda anpassat tabbstopp. [TabStop](./)-objektet är en medlem av [TabStopCollection](../tabstopcollection/)-samlingen. För att lära dig mer, besök dokumentationsartikeln [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class TabStop : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Jämför med den angivna [TabStop](./). |
| [get_Alignment](./get_alignment/)() const | Hämtar eller anger justeringen av text vid detta tabbstopp. |
| [get_IsClear](./get_isclear/)() | Returnerar **true** om detta tabbstopp rensar eventuella befintliga tabbstopp på den här positionen. |
| [get_Leader](./get_leader/)() const | Hämtar eller anger typen av ledarlinje som visas under tabulatortecknet. |
| [get_Position](./get_position/)() | Hämtar positionen för tabbstoppet i punkter. |
| [GetHashCode](./gethashcode/)() const override | Beräknar hashkod för detta objekt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::TabAlignment) | Sättare för [Aspose::Words::TabStop::get_Alignment](./get_alignment/). |
| [set_Leader](./set_leader/)(Aspose::Words::TabLeader) | Sättare för [Aspose::Words::TabStop::get_Leader](./get_leader/). |
| [TabStop](./tabstop/)(double) | Initierar en ny instans av den här klassen. |
| [TabStop](./tabstop/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Initierar en ny instans av den här klassen. |
| static [Type](./type/)() |  |
## Anmärkningar


Normalt anger ett tabbstopp en position där ett tabbstopp finns. Men eftersom tabbstopp kan ärvas från förälderstilar kan det vara nödvändigt för det underordnade objektet att uttryckligen definiera att det inte finns något tabbstopp på en given position. För att rensa ett ärvt tabbstopp på en given position, skapa ett [TabStop](./)-objekt och sätt [Alignment](./get_alignment/) till [Clear](../tabalignment/).

För mer information, se [TabStopCollection](../tabstopcollection/).

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
