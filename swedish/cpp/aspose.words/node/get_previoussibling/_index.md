---
title: "Aspose::Words::Node::get_PreviousSibling metod"
linktitle: "get_PreviousSibling"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Node::get_PreviousSibling metod. Hämtar noden som omedelbart föregår denna nod i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words/node/get_previoussibling/
---
## Node::get_PreviousSibling method


Hämtar noden som omedelbart föregår den här noden.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_PreviousSibling()
```


## Exempel



Visar hur man använder metoderna i [Node](../) och [CompositeNode](../../compositenode/) för att ta bort ett avsnitt före det sista avsnittet i dokumentet.
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

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
