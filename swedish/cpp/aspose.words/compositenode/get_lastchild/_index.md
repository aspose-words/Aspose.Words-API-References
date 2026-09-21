---
title: "Aspose::Words::CompositeNode::get_LastChild‑metod"
linktitle: "get_LastChild"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::CompositeNode::get_LastChild‑metod. Hämtar den sista barnet till noden i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/compositenode/get_lastchild/
---
## CompositeNode::get_LastChild method


Hämtar det sista barnet till noden.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::get_LastChild() const
```


## Exempel



Visar hur man använder metoderna i [Node](../../node/) och [CompositeNode](../) för att ta bort ett avsnitt före det sista avsnittet i dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1 text.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Writeln(u"Section 2 text.");

// Båda avsnitten är syskon till varandra.
auto lastSection = System::ExplicitCast<Aspose::Words::Section>(doc->get_LastChild());
auto firstSection = System::ExplicitCast<Aspose::Words::Section>(lastSection->get_PreviousSibling());

// Ta bort ett avsnitt baserat på dess syskonrelation med ett annat avsnitt.
if (lastSection->get_PreviousSibling() != nullptr)
{
    doc->RemoveChild<System::SharedPtr<Aspose::Words::Section>>(firstSection);
}

// Avsnittet vi tog bort var det första, vilket lämnade dokumentet med endast det andra.
ASSERT_EQ(u"Section 2 text.", doc->GetText().Trim());
```

## Se även

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
