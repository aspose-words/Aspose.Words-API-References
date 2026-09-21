---
title: "Aspose::Words::Range::get_Text‑metod"
linktitle: "get_Text"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Range::get_Text‑metod. Hämtar texten för området i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/range/get_text/
---
## Range::get_Text method


Hämtar texten i området.

```cpp
System::String Aspose::Words::Range::get_Text()
```

## Anmärkningar


Den returnerade strängen inkluderar alla kontroll- och specialtecken som beskrivs i [ControlChar](../../controlchar/).

## Exempel



Visar hur man hämtar textinnehållet för alla noder som ett område täcker.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## Se även

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
