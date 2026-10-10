---
title: "Aspose::Words::Section::get_Body method"
linktitle: "get_Body"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Section::get_Body method. Returnerar Body-underordnad nod för avsnittet i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words/section/get_body/
---
## Section::get_Body method


Returnerar den [Body](../../body/) underordnade noden för avsnittet.

```cpp
System::SharedPtr<Aspose::Words::Body> Aspose::Words::Section::get_Body()
```

## Anmärkningar


[Body](../../body/) contains main text of the section.

Returnerar **null** om avsnittet inte har en [Body](../../body/) nod bland sina barn.

## Exempel



Rensar huvudtexten från alla sektioner i dokumentet och lämnar sektionerna själva.
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

// Ett avsnitt behöver en kropp, som kommer att innehålla och visa allt dess innehåll
// på sidan mellan avsnittets sidhuvud och sidfot.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Denna kropp har inga barn, så vi kan ännu inte lägga till runs i den.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Anropa "EnsureMinimum" för att säkerställa att denna kropp innehåller minst ett tomt stycke.
body->EnsureMinimum();

// Nu kan vi lägga till runs i kroppen och få dokumentet att visa dem.
body->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Se även

* Class [Body](../../body/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
