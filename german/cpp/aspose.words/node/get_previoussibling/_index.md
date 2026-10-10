---
title: "Aspose::Words::Node::get_PreviousSibling-Methode"
linktitle: "get_PreviousSibling"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Node::get_PreviousSibling-Methode. Gibt den Knoten zurück, der diesem Knoten in C++ unmittelbar vorausgeht."
type: docs
weight: 11000
url: /de/cpp/aspose.words/node/get_previoussibling/
---
## Node::get_PreviousSibling method


Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_PreviousSibling()
```


## Beispiele



Zeigt, wie man die Methoden von [Node](../) und [CompositeNode](../../compositenode/) verwendet, um einen Abschnitt vor dem letzten Abschnitt im Dokument zu entfernen.
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

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
