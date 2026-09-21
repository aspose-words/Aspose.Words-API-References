---
title: "Aspose::Words::Rendering::PageInfo::get_Colored metod"
linktitle: "get_Colored"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Rendering::PageInfo::get_Colored metod. Returnerar true om sidan innehåller färgat innehåll i C++."
type: docs
weight: 1500
url: /sv/cpp/aspose.words.rendering/pageinfo/get_colored/
---
## PageInfo::get_Colored method


Returnerar **true** om sidan innehåller färgat innehåll.

```cpp
bool Aspose::Words::Rendering::PageInfo::get_Colored()
```


## Exempel



Visar hur man kontrollerar om sidan är i färg eller inte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Kontrollera att den första sidan i dokumentet inte är färgad.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## Se även

* Class [PageInfo](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
