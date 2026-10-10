---
title: "Aspose::Words::Body::Body konstruktor"
linktitle: "Body"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Body::Body konstruktor. Initierar en ny instans av Body-klassen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/body/body/
---
## Body::Body constructor


Initierar en ny instans av klassen [Body](../).

```cpp
Aspose::Words::Body::Body(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Ägandokumentet. |
## Anmärkningar


När [Body](../) skapas, tillhör den det angivna dokumentet, men är ännu inte en del av dokumentet och [ParentNode](../../node/get_parentnode/) är **null**.

För att lägga till [Body](../) till en [Section](../../section/) använd metoderna [AppendChild](../)[InsertAfter](../) eller [InsertBefore](../).

## Exempel



Visar hur man konstruerar ett Aspose.Words-dokument för hand.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ett tomt dokument innehåller ett avsnitt, en kropp och ett stycke.
// Anropa metoden "RemoveAllChildren" för att ta bort alla dessa noder,
// och sluta med ett dokumentnod utan barn.
doc->RemoveAllChildren();

// Detta dokument har nu inga sammansatta barnnoder som vi kan lägga till innehåll i.
// Om vi vill redigera det måste vi återfylla dess nodsamling.
// Först, skapa ett nytt avsnitt och lägg sedan till det som ett barn till rot-dokumentnoden.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Ställ in några sidinställningsegenskaper för avsnittet.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Ett avsnitt behöver en kropp, som kommer att innehålla och visa allt dess innehåll
// på sidan mellan avsnittets sidhuvud och sidfot.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Skapa ett stycke, ställ in några formateringsegenskaper och lägg sedan till det som ett barn till kroppen.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Slutligen, lägg till lite innehåll för att skapa dokumentet. Skapa ett run,
// ställ in dess utseende och innehåll, och lägg sedan till det som ett barn till stycket.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Se även

* Class [DocumentBase](../../documentbase/)
* Class [Body](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
