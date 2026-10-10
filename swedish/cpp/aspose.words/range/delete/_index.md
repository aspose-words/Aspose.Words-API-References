---
title: "Aspose::Words::Range::Delete metod"
linktitle: "Ta bort"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Range::Delete metod. Raderar alla tecken i intervallet i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/range/delete/
---
## Range::Delete method


Raderar alla tecken i området.

```cpp
void Aspose::Words::Range::Delete()
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

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
