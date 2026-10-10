---
title: "Aspose::Words::Node::get_Range metod"
linktitle: "get_Range"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Node::get_Range metod. Returnerar ett Range‑objekt som representerar den del av ett dokument som finns i denna nod i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words/node/get_range/
---
## Node::get_Range method


Returnerar ett [Range](../../range/)‑objekt som representerar den del av ett dokument som finns i denna nod.

```cpp
System::SharedPtr<Aspose::Words::Range> Aspose::Words::Node::get_Range()
```


## Exempel



Visar hur man tar bort alla noder från ett range.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Lägg till text i det första avsnittet i dokumentet och lägg sedan till ett annat avsnitt.
builder->Write(u"Section 1. ");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Write(u"Section 2.");

ASSERT_EQ(u"Section 1. \fSection 2.", doc->GetText().Trim());

// Ta bort det första avsnittet helt genom att ta bort alla noder
// inom dess range, inklusive avsnittet självt.
doc->get_Sections()->idx_get(0)->get_Range()->Delete();

ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(u"Section 2.", doc->GetText().Trim());
```

## Se även

* Class [Range](../../range/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
