---
title: "Aspose::Words::Run class"
linktitle: "Run"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Run class. Representerar en sekvens av tecken med samma teckensnittsformatering. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 56000
url: /sv/cpp/aspose.words/run/
---
## Run class


Representerar en sekvens av tecken med samma teckensnittsformatering. För att lära dig mer, besök dokumentationsartikeln [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Run : public Aspose::Words::Inline
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare. |
| [Clone](../node/clone/)(bool) | Skapar en kopia av noden. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| virtual [get_Document](../node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_Font](../inline/get_font/)() | Tillhandahåller åtkomst till teckensnittsformateringen för detta objekt. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Returnerar **true** om denna nod kan innehålla andra noder. |
| [get_IsDeleteRevision](../inline/get_isdeleterevision/)() | Returnerar true om detta objekt raderades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsFormatRevision](../inline/get_isformatrevision/)() | Returnerar true om formateringen av objektet ändrades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsInsertRevision](../inline/get_isinsertrevision/)() | Returnerar true om detta objekt infogades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveFromRevision](../inline/get_ismovefromrevision/)() | Returnerar **true** om detta objekt flyttades (raderades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveToRevision](../inline/get_ismovetorevision/)() | Returnerar **true** om detta objekt flyttades (infogades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsPhoneticGuide](./get_isphoneticguide/)() | Hämtar ett booleskt värde som indikerar om körningen är en fonetisk guide. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| [get_NodeType](./get_nodetype/)() const override | Returnerar [Run](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_ParentParagraph](../inline/get_parentparagraph/)() | Hämtar föräldern [Paragraph](../paragraph/) till denna nod. |
| [get_PhoneticGuide](./get_phoneticguide/)() | Hämtar ett [PhoneticGuide](./get_phoneticguide/)‑objekt. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Returnerar ett [Range](../range/)-objekt som representerar den del av ett dokument som finns i den här noden. |
| [get_Text](./get_text/)() const | Hämtar eller anger texten för körningen. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern till den angivna [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetText](./gettext/)() override | Hämtar texten för run. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar nästa nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | En hjälpfunktion som konverterar ett nodtyp‑enumvärde till en användarvänlig sträng. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar föregående nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| [Remove](../node/remove/)() | Tar bort sig själv från föräldern. |
| [Run](./run/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initierar en ny instans av klassen [Run](./). |
| [Run](./run/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) | Initierar en ny instans av klassen **Run**. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Sättare för [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Text](./set_text/)(const System::String\&) | Sättare för [Aspose::Words::Run::get_Text](./get_text/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
## Anmärkningar


All text of the document is stored in runs of text.

[Run](./) can only be a child of [Paragraph](../paragraph/) or inline [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).

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


Visar hur man lägger till, uppdaterar och tar bort barnnoder i en [CompositeNode](../compositenode/)'s samling av barn.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ett tomt dokument har som standard ett stycke.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Sammansatta noder såsom vårt stycke kan innehålla andra sammansatta och inline‑noder som barn.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// Skapa tre ytterligare run‑noder.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// Dokumentkroppen kommer inte att visa dessa runs förrän vi infogar dem i en sammansatt nod
// som i sig är en del av dokumentets nodträd, precis som vi gjorde med den första run‑en.
// Vi kan bestämma var textinnehållet i noder som vi infogar
// visas i dokumentet genom att ange en infogningsplats relativt en annan nod i stycket.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// Infoga den andra run‑en i stycket framför den ursprungliga run‑en.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Infoga den tredje run‑en efter den ursprungliga run‑en.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// Infoga den första run‑en i början av styckets samling av barnnoder.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Vi kan ändra innehållet i run‑en genom att redigera och ta bort befintliga barnnoder.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```


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

* Class [Inline](../inline/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
