---
title: "Aspose::Words::Run::Run konstruktor"
linktitle: "Run"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Run::Run konstruktor. Initierar en ny instans av Run‑klassen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/run/run/
---
## Run::Run(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) constructor


Initierar en ny instans av klassen [Run](../).

```cpp
Aspose::Words::Run::Run(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Ägandokumentet. |
## Anmärkningar


När [Run](../) skapas tillhör den det angivna dokumentet, men är ännu inte en del av dokumentet och [ParentNode](../../node/get_parentnode/) är **null**.

För att lägga till [Run](../) i dokumentet, använd [InsertAfter1()</see> or <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) på det stycke där du vill att runen infogas.

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
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Run::Run(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) constructor


Initierar en ny instans av klassen **Run**.

```cpp
Aspose::Words::Run::Run(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, const System::String &text)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Ägandokumentet. |
| text | const System::String\& | Texten för runen. |
## Anmärkningar


När [Run](../) skapas tillhör den det angivna dokumentet, men är ännu inte en del av dokumentet och [ParentNode](../../node/get_parentnode/) är **null**.

För att lägga till [Run](../) i dokumentet, använd [InsertAfter1()</see> or <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) på det stycke där du vill att runen infogas.

## Exempel



Visar hur man formaterar en run av text med dess font‑egenskap.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Se även

* Class [DocumentBase](../../documentbase/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
