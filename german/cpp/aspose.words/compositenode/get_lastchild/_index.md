---
title: "Aspose::Words::CompositeNode::get_LastChild Methode"
linktitle: "get_LastChild"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::CompositeNode::get_LastChild Methode. Gibt das letzte untergeordnete Element des Knotens in C++ zurück."
type: docs
weight: 8000
url: /de/cpp/aspose.words/compositenode/get_lastchild/
---
## CompositeNode::get_LastChild method


Ermittelt das letzte Kind des Knotens.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::get_LastChild() const
```


## Beispiele



Zeigt, wie die Methoden von [Node](../../node/) und [CompositeNode](../) verwendet werden, um einen Abschnitt vor dem letzten Abschnitt im Dokument zu entfernen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1 text.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Writeln(u"Section 2 text.");

// Beide Abschnitte sind Geschwister zueinander.
auto lastSection = System::ExplicitCast<Aspose::Words::Section>(doc->get_LastChild());
auto firstSection = System::ExplicitCast<Aspose::Words::Section>(lastSection->get_PreviousSibling());

// Entferne einen Abschnitt basierend auf seiner Geschwisterbeziehung zu einem anderen Abschnitt.
if (lastSection->get_PreviousSibling() != nullptr)
{
    doc->RemoveChild<System::SharedPtr<Aspose::Words::Section>>(firstSection);
}

// Der entfernte Abschnitt war der erste, sodass das Dokument nur noch den zweiten enthält.
ASSERT_EQ(u"Section 2 text.", doc->GetText().Trim());
```

## Siehe auch

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
