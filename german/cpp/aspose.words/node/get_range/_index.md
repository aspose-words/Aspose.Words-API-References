---
title: "Aspose::Words::Node::get_Range Methode"
linktitle: "get_Range"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Node::get_Range-Methode. Gibt ein Range-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist, in C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words/node/get_range/
---
## Node::get_Range method


Gibt ein [Range](../../range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist.

```cpp
System::SharedPtr<Aspose::Words::Range> Aspose::Words::Node::get_Range()
```


## Beispiele



Zeigt, wie man alle Knoten aus einem Bereich löscht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Füge Text zum ersten Abschnitt im Dokument hinzu und füge dann einen weiteren Abschnitt hinzu.
builder->Write(u"Section 1. ");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Write(u"Section 2.");

ASSERT_EQ(u"Section 1. \fSection 2.", doc->GetText().Trim());

// Entferne den ersten Abschnitt vollständig, indem du alle Knoten entfernst
// innerhalb seines Bereichs, einschließlich des Abschnitts selbst.
doc->get_Sections()->idx_get(0)->get_Range()->Delete();

ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(u"Section 2.", doc->GetText().Trim());
```

## Siehe auch

* Class [Range](../../range/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
