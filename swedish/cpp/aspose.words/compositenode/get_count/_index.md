---
title: "Aspose::Words::CompositeNode::get_Count‑metod"
linktitle: "get_Count"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::CompositeNode::get_Count‑metod. Hämtar antalet omedelbara barn till denna nod i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/compositenode/get_count/
---
## CompositeNode::get_Count method


Hämtar antalet omedelbara barn till denna nod.

```cpp
int32_t Aspose::Words::CompositeNode::get_Count()
```


## Exempel



Visar hur man lägger till, uppdaterar och tar bort barnnoder i en [CompositeNode](../)s samling av barn.
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

## Se även

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
